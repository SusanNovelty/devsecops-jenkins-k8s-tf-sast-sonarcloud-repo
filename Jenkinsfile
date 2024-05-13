pipeline {
  agent any
  tools { 
        maven 'Maven_3.5.2'  
    }
   stages{
    stage(‘Checkout’) {
			steps {
				// Checkout the repository  from GitHub
				git  url: ‘https://github.com/SusanNovelty/devsecops-jenkins-k8s-tf-sast-sonarcloud-repo.git'
			}
		}
    stage('CompileandRunSonarAnalysis') {
            steps {	
		sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=buggywebappsusan -Dsonar.organization=buggywebappsusan -Dsonar.host.url=https://sonarcloud.io -Dsonar.token=49e45bc6ac9c13528ff3b7a0117ae99e21b497df'}
        } 
  }
}
