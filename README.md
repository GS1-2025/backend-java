# ☀ Sensolux

## 👨‍💻 Integrantes
- RM558763 • Eric Issamu de Lima Yoshida  
- RM555010 • Gustavo Matias Teixeira  
- RM557515 • Gustavo Monção  

## 💬 Vídeo Pitch  
[Youtube](https://youtu.be/WJmfimRwF8w)  

## 💬 Vídeo demonstrando o funcionamento  
[Youtube](https://youtu.be/M-hwVPVmYOA?si=GZY7YPaV2qzo3apV)  

## 🔌 Circuito no Wokwi  
[Wokwi](https://wokwi.com/projects/432380308913932289)  

## 📈 Thingspeak  
[Thingspeak](https://thingspeak.mathworks.com/channels/2975872)  

---

## 🛠 Funcionamento do projeto
1. Rode o circuito no Wokwi.  
2. Simule temperaturas e índices UV através dos sensores do circuito.  
3. Verifique as mudanças no Thingspeak.  
4. As informações são enviadas para a aplicação backend Java, que disponibiliza uma API REST para acessar e manipular esses dados.  

---

## 💻 Tecnologias utilizadas
- Java 17 + Spring Boot  
- Spring Security (JWT para autenticação)  
- Banco de dados relacional (ex: PostgreSQL ou MySQL)  
- Wokwi para simulação do circuito  
- Thingspeak para armazenamento e visualização de dados IoT  
- REST API para comunicação frontend/backend  

---

## 🔍 Endpoints da API

| Endpoint                      | Método  | Descrição                                                       |
|------------------------------|---------|-----------------------------------------------------------------|
| `/auth/login`                 | POST    | Realiza login e retorna token JWT                               |
| `/auth/register`              | POST    | Registro de novo usuário                                        |
| `/auth/recover-password`      | POST    | Solicita recuperação de senha, envia link com token            |
| `/auth/reset-password`        | POST    | Redefine senha usando token de recuperação                      |
| `/dados`                     | GET     | Retorna dados dos sensores (restrito a usuários autenticados)  |
| `/dados/publico`              | GET     | Dados públicos disponíveis sem autenticação                     |
| `/dados/{id}`                | GET     | Retorna dado específico por ID                                  |
| `/usuario`                   | GET     | Informações do usuário autenticado                              |
| `/usuario/sensores`          | GET     | Dados dos sensores associados ao usuário                        |
| `/alertas`                   | GET     | Lista de alertas (usuário recebe alertas)                      |
| `/alertas/{id}`              | GET     | Detalhes de alerta específico                                  |
| `/dashboard/average-humidity-today` | GET | Média da umidade do dia atual                                  |
| `/dashboard/average-temperature-today` | GET | Média da temperatura do dia atual                            |
| `/dashboard/between`         | GET     | Dados entre duas datas específicas                              |
| `/dashboard/latest`          | GET     | Últimos dados registrados                                      |
| `/error`                     | GET     | Endpoint para tratamento de erros                              |

---

## 🚀 Como rodar o projeto

### Backend
1. Configure seu banco de dados (MySQL, PostgreSQL ou outro).  
2. Atualize o arquivo `application.properties` com as credenciais do banco .  
3. Rode o projeto Spring Boot (`./mvnw spring-boot:run` ou pelo seu IDE favorito).  

### Frontend / IoT
1. Acesse o circuito no Wokwi e rode a simulação.  
2. Os dados simulados serão enviados automaticamente para Thingspeak e para o backend via API.  
3. Teste os endpoints com ferramentas como Postman ou Insomnia.  

---

