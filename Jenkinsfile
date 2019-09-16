pipeline {
agent any

tools {
jdk "Java-1.8"
maven "Maven-3.5.3"
}

stages {
    stage('Clone repo'){
    steps{
    git url: 'https://github.com/Izual10/DemoDevOps'
    }
    }
  }

}
