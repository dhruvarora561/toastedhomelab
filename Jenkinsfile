pipeline {
agent any 
stages {

    stage ("init") {
        steps {
        echo "initializing pipeline"
        }
    }
    stage ('build') {
        steps {
        echo "building the pipeline"
        }
    }
    stage('SonarQube Analysis') {
        steps {
    def scannerHome = tool 'SonarScanner';
    withSonarQubeEnv() {
      sh "${scannerHome}/bin/sonar-scanner"
    }
        }
  }
    stage ('deployment') {
        steps {
        echo "deployment completed"
        }
    }
}
}

