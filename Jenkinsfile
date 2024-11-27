pipeline { 
    agent any 
    stages { 
        stage("Checkout /Clone from Git & Maven Build") { 
            steps { 
                      git branch: "Main" ,   url : "https://github.com/devopsusergit/PetStoreWebApp.git"
                      sh  'mvn clean'
                      sh  ' mvn package'
            } 
        } 
        stage('Clean and Package') {
        steps {
        echo 'Cleaning workspace and packaging'
        sh 'mvn clean package'

        }

        }
        stage('Stage 1') {
      steps {
        script {
          echo 'This is for stage 3 assessment.'
        }
      }
    }
        stage('Parallel Tasks') {
              parallel {
              stage('Regression and Acceptance Tests') {
       stages {
        stage('Regression Testing') {
        steps {
        echo 'Running regression tests...'
    }
  }
     stage('Acceptance Testing') {
        steps {
        echo 'Running acceptance tests...'
}
}
}
}  
}
        }
    }
}
