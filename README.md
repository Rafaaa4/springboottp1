# 📦 Projet Spring Boot - Gestion des Utilisateurs

## 📖 Description
Ce projet est une application web développée avec Spring Boot permettant de gérer des utilisateurs via une API REST.

Fonctionnalités :
- Création d’un utilisateur
- Consultation des utilisateurs
- Suppression d’un utilisateur

---

## 🏗️ Architecture
src/main/java/com/example/springbootdb/
│
├── controller/
├── service/
├── repository/
├── model/
└── SpringbootDbApplication.java

---

## ⚙️ Configuration

### H2 Database
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.driverClassName=org.h2.Driver
spring.datasource.username=sa
spring.datasource.password=password
spring.jpa.database-platform=org.hibernate.dialect.H2Dialect
spring.h2.console.enabled=true


---

## 📦 Dépendances

- Spring Boot Starter Web
- Spring Boot Starter Data JPA
- MySQL Connector
- H2 Database

---

## 🧱 Entité Utilisateur

```java
@Entity
public class Utilisateur {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;
    private String nom;
    private String email;
}
```
---

🔌 API REST
Base URL
http://localhost:8080/api/utilisateurs
Endpoints
GET / → Liste des utilisateurs
GET /{id} → Détails utilisateur
POST / → Ajouter utilisateur
DELETE /{id} → Supprimer utilisateur

🧪 Exemple POST
```
{
  "nom": "Jean Dupont",
  "email": "jean.dupont@example.com"
}
```
▶️ Lancer le projet
```
git clone <repo_url>
```
Lancer l’application :
```
mvn spring-boot:run
```
Ou exécuter :

SpringbootDbApplication.java

Accéder à l’application :

http://localhost:8080
🛠️ Outils
Postman
IntelliJ IDEA / VS Code
MySQL Workbench
🚀 Améliorations possibles
Authentification JWT
Validation des données
Pagination
Gestion des erreurs globale
