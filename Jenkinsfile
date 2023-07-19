pipeline {
    agent any

    tools {
          maven 'Maven 3.9.3'
    }

    stages {
        stage('Code Clone') {
            steps {
               git credentialsId: 'git', url: 'https://github.com/ksrepo9/ks.git'
            }
			}
		stage('Maven Version') {
            steps {
               sh 'mvn --version'
            }
			}	
		stage('Maven Clean') {
            steps {
               sh 'mvn clean'
            }
			}
				stage('Maven Validate') {
            steps {
               sh 'mvn validate'
            }
			}
				stage('Maven Compile') {
            steps {
               sh 'mvn compile'
            }
			}
		stage('Maven Test') {
            steps {
               sh 'mvn test'
            }
			}
		stage('Maven Package') {
            steps {
               sh 'mvn package'
            }
			}			

   }
}
