pipeline {
    agent any

    environment {
        // Use PATH+EXTRA to append to PATH properly
        PATH = "/opt/gradle/latest/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin"
    }

    stages {

        stage('pull') {
            steps {

 branch: 'feature', url: 'https://github.com/skbasha-devops/Amazon-Jenkins'

             

              



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
