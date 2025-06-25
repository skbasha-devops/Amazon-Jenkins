pipeline {
    agent any
    stages {

        stage('pull') {
            steps {
                git branch: 'feature', url: 'https://github.com/skbasha-devops/Amazon-Jenkins'
            }
        }

        stage('compile') {
            steps {
                sh 'mvn compile'
            }
        }

        stage('build') {
            steps {
                 sh 'mvn clean install'
            }
        }


    }

  post{
    
  failure{
       echo 'Failure in the build'
   }

  }


}
