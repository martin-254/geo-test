pipeline{
    agent any
    
    
    stages{
        stage('maven clean') {
        steps{
            sh ' /opt/maven/lib/mvn clean'
        }
        }
        stage('maven install'){
        steps{
            sh '/opt/maven/lib/mvn install'
        }
    }
    stage('maven package'){
        steps{
            sh '/opt/maven/lib/mvn package'
    
        }
    }

    }
}
    
