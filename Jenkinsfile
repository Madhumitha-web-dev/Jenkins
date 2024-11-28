pipeline { 
    agent any 
    stages { 
        stage("Checkout") { 
            steps { 
                      git branch: "Main" ,   url : "https://github.com/devopsusergit/PetStoreWebApp.git"
                      sh  'mvn clean'
                      sh  ' mvn package'
            } 
        } 
        stage('Clean Package') {
        steps {
        echo 'Cleaning workspace and packaging'
        sh 'mvn clean package'

        }

        }


        stage('Test stage') {
      steps {
        script {
          echo 'This is for stage 3 assessment.'
        }
      }
    }
        
    
        stage('Performance Testing') {
                parallel {
            steps{
            echo 'Running performance tests'
          }
            
       stage('Code Quality Check') {
         steps {
         echo 'Running code quality checks'
         }
        }
        stage('Regression and Acceptance testing'){
         stages{          
        stage('Regression Testing') {
        steps {
        echo 'Running regression tests'
    }
  }
     stage('Acceptance Testing') {
        steps {
        echo 'Running acceptance tests'
       }
      }
     }
    }  
        }
    }
}
}


                                                            






                                                       
