pipeline{
    agent any
    tools{
        maven 'M2_HOME'
    }
    stages{
        stage('maven clean') {
        steps{
            sh ' mvn clean'
        }
        }
        stage('maven install'){
        steps{
            sh 'mvn install'
        }
    }
    stage('maven package'){
        steps{
            sh 'mvn package'
    
        }
    }
    stage('upload artifact') {
        steps{nexusArtifactUploader artifacts: 
        [[artifactId: '${POM_GROUPID}', 
        classifier: '', 
        file: 'target/${POM_GROUPID}-${POM_VERSION}.${POM_PACKAGE}', 
        type: '${POM_PACKAGE}']], 
        credentialsId: 'jenkins-user-credentials', 
        groupId: '${POM_GROUPID}', 
        nexusUrl: 'ec2-13-59-42-35.us-east-2.compute.amazonaws.com:8081', 
        nexusVersion: 'nexus3', 
        protocol: 'http', 
        repository: 'geo-test', 
        version: ' ${POM_VERSION}'}
    }
}
    
}