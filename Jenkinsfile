node {
    stage('Code Clone') { 	
	  git credentialsId: 'git', url: 'https://github.com/ksrepo9/ks.git'
	 }
    stage('Code Clean') {
      sh 'mvn clean'
    }
    stage('Maven Validate') {
      sh 'mvn validate'
    }
	stage('Maven Compile'){
	  sh 'mvn compile' 
	  }
	stage('Maven Test'){
	  sh 'mvn test'
	}
	stage('Maven Package'){
	  sh 'mvn package'
	}
}
