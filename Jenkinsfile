pipeline {
    agent any

    tools {
          maven 'Apache Maven 3.9.3'
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
		stage('Sonar Scan'){
            steps {
             
			  sh 'mvn sonar:sonar -Dsonar.host.url=http://192.168.29.19:9000 -Dsonar.login=1bac12cfa5e6f7a218ab205d18301e6cfbb89e3f'
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
		stage('Maven Deploy') {
            steps {
               sh 'mvn deploy'
            }
			}			

   }
}
