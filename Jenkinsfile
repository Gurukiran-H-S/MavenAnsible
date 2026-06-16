pipeline {
    agent any  // Use any available agent
    tools {
        maven 'Maven'  // Ensure this matches the name configured in Jenkins
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Gurukiran-H-S/MavenAnsible.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'  // Run Maven build
            }
        }

        stage('Deploy') {
            steps {
               sh 'mvn clean package'  
               sh 'ansible-playbook playbook.yml -i hosts.ini'
            }
        }

                  
    }

   }
