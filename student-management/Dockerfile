# On utilise une image légère juste pour RUN (pas besoin de Maven ici)
FROM eclipse-temurin:17-jre-alpine

WORKDIR /app

# On copie le JAR qui a été généré par Jenkins juste avant (à l'étape 2 du pipeline)
# Le chemin "target/*.jar" correspond à l'endroit où Maven dépose le fichier
COPY target/*.jar app.jar

# On expose le port 8089 (celui utilisé dans ton service Kubernetes)
EXPOSE 8089

# Lancement de l'application
ENTRYPOINT ["java", "-jar", "app.jar"]
