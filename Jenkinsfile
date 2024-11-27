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
        echo 'Cleaning workspace and packaging_
        sh 'mvn clean package'

        }

        }
     }  
}
