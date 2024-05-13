pipeline {
  agent any
  tools { 
        maven 'Maven_3_5_2'  
    }
   stages{
    stage('CompileandRunSonarAnalysis') {
            steps {	
		sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=buggywebappsusan -Dsonar.organization=buggywebappsusan -Dsonar.host.url=https://sonarcloud.io -Dsonar.token=5e2166d612700c1b2ae24971dbbb2d038f870092'
			}
        } 
  }
}
