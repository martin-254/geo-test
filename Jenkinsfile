pipeline{
    agent any
    
    
    stages{
        stage('maven clean') {
        steps{
            sh ' /var/maven/lib/mvn clean'
        }
        }
        stage('maven install'){
        steps{
            sh '/var/maven/lib/mvn install'
        }
    }
    stage('maven package'){
        steps{
            sh '/var/maven/lib/mvn package'
    
        }
    }

    }
}
    
