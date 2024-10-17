pipeline {
    agent any

    environment{
        AUTHOR = "Ahmad Hafid"
        EMAIL = "ahmadhafid.tech@gmail.com"
        WEB = "https://ocinz.tech"
    }

    stages{
        stage("Prepare"){
            step{
                echo( "Hello World")
                echo( "Prepare Stage")
                echo( "Author: ${AUTHOR} ")
            }
        }
        stage("Build"){
            step{
                echo "Hello World"
                echo "Build Stage"
                echo "Author: ${EMAIL}"
            }
        }`
        stage("Test"){
            step{
                echo "Hello World"
                echo "Test Stage"
                echo "Author: ${WEB}"
            }
        }
    }
}