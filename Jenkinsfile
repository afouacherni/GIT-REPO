pipeline {
    agent any
    tools {
        // Assurez-vous que JDK21 est bien configuré dans 'Gérer Jenkins -> Outils globaux'
        jdk 'JDK-17' 
    }
    
    stages {
        stage('Checkout code') {
            steps {
                // Remplacez 'https://github.com/Jamina-ENSI/Hello_example.git' par l'URL de votre dépôt
                git branch: 'main', url: 'https://github.com/afouacherni/GIT-REPO.git'
            }
        }
        
        stage('Compile code') {
            steps {
                // Compilation: trouve le fichier source dans src/application
                sh 'javac src/application/Test.java' 
            }
        }
        
        stage('Execute code') {
            steps {
                // Exécution: utilise le sous-dossier src/application comme classpath
                sh 'java -cp src/application Test' 
            }
        }
    }
}
