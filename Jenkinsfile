pipeline{
    agent{
        label 'java-build-server'
    }
    stages{
        stage('SCM checkout'){
            steps{
                git url: 'https://github.com/spring-projects/spring-petclinic.git', branch: 'main'
            }
        }
        stage('maven build'){
            steps{
                sh 'mvn clean package'
            }
        }
        stage('reporting'){
            steps{
                junit testResults: 'target/surefire-reports/*.xml'
            }
        }
    }
}