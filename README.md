# student-api

API REST Spring Boot pour la gestion d'étudiants — TP Intégration Continue avec Jenkins.

**Module** : Livraison Continue (2IDA2103) — Master 1 UNCHK  
**Auteur** : Dr. Mouhamadou Lamine DIAKHAME

## Prérequis

- Java 17
- Maven 3.9

## Lancer le projet

```bash
mvn spring-boot:run
```

## Exécuter les tests

```bash
mvn clean test
```

## Vérifier la couverture (seuil 70 %)

```bash
mvn verify
```

## Endpoints

| Méthode | URL                    | Description              |
|---------|------------------------|--------------------------|
| GET     | /api/students          | Liste tous les étudiants |
| GET     | /api/students/{id}     | Récupère un étudiant     |
| POST    | /api/students          | Crée un étudiant         |
| DELETE  | /api/students/{id}     | Supprime un étudiant     |

## Exemple de requête POST

```json
{
  "nom": "Diop",
  "prenom": "Awa",
  "email": "awa@uvs.sn",
  "moyenne": 14.5
}
```
# Student API 

Une API REST robuste pour la gestion des étudiants, développée avec Spring Boot et entièrement intégrée dans un pipeline de déploiement continu (CI/CD).

## Technologies Utilisées
* **Backend :** Java / Spring Boot
* **Gestion de base de données :** Spring Data JPA
* **Tests & Qualité :** JUnit, Jacoco (Rapports de couverture)

## Pipeline CI/CD (DevOps)
Ce projet intègre les bonnes pratiques de l'intégration continue :
1. **Versionnage :** Hébergé sur GitHub.
2. **Webhook :** Déclenchement automatique des builds à chaque `git push` via un tunnel **ngrok**.
3. **Serveur d'intégration :** Compilé, testé et vérifié automatiquement par **Jenkins**.
