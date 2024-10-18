pipeline {
    agent any

    environment{
        AUTHOR = "Ahmad Hafid"
        EMAIL = "ahmadhafid.tech@gmail.com"
        WEB = "https://ocinz.tech"
    }

    parameters {
    string(name: "NAME", defaultValue: "Guest", description: "What is your name?")
    text(name: "DESCRIPTION", defaultValue: "Guest", description: "Tell me about you")
    booleanParam(name: "DEPLOY", defaultValue: false, description: "Need to Deploy?")
    choice(name: "SOCIAL_MEDIA", choices: ['Instagram', 'Facebook', 'Twitter'], description: "Which Social Media?")
    password(name: "SECRET", defaultValue: "", description: "Encrypt Key")
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
              sleep(time: 10, unit: 'SECONDS')
                echo "Hello World"
                echo "Build Stage"
                echo "Email: ${EMAIL}"
            }
        }
        stage("Parameter") {
          steps {
            echo "Hello ${params.NAME}"
            echo "You description is ${params.DESCRIPTION}"
            echo "Your social medis is ${params.SOCIAL_MEDIA}"
            echo "Need to deploy : ${params.DEPLOY} to deploy!"
            echo "Your secret is ${params.SECRET}"
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