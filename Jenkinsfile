pipeline{
    agent{
        label 'centos-jdk-17'
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