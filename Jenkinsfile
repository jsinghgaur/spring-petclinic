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
        stage('test'){
            steps{
                sh '/opt/apache-maven-3.9.0/bin/mvn clean test'
            }
        }
    }
}