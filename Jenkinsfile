pipeline {
    agent any

    environment{
        AUTHOR = "Ahmad Hafid"
        EMAIL = "ahmadhafid.tech@gmail.com"
        WEB = "https://ocinz.tech"
    }

    options {
      disableConcurrentBuilds()
      timeout(time: 10, unit: 'MINUTES')
    }

    stages{
        stage("Prepare"){
            steps{
                echo( "Hello World")
                echo( "Prepare Stage")
                echo( "Author: ${AUTHOR} ")
            }
        }
        stage("Build"){
            steps{
                echo "Hello World"
                echo "Build Stage"
                echo "Email: ${EMAIL}"
            }
        }
        stage("Test"){
            steps{
                echo "Hello World"
                echo "Test Stage"
                echo "Web: ${WEB}"
            }
        }
    }

  post {
    always {
      echo "I will always say Hello again!"
    }
    success {
      echo "Yay, success"
    }
    failure {
      echo "Oh no, failure"
    }
    cleanup {
      echo "Don't care success or error"
    }
  }
}