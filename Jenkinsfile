pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven_3_6_2') {
                    sh 'mvn clean install'
                }
            }
        }

		stage('SonarQube analysis') {
    def scannerHome = tool 'SonarScanner 4.0';
    withSonarQubeEnv('http://192.168.56.51:9000') { 
      sh "${scannerHome}/bin/sonar-scanner"
    }
  }
       


        
        }
    }
