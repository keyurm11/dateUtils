pipeline {
    agent any
    
    tools{
        maven 'mvn_home'
    }

    stages {
        stage ('Packaging and Distribution') {
            steps {
                withMaven(maven : 'mvn_home') {
                    sh 'mvn clean package'
                }
            }
        }
        
        stage ('Archive Artifacts') {
            steps {
                archiveArtifacts 'target/*.jar'
            }
        }
    }
}
