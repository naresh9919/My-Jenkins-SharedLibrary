# My-Jenkins-SharedLibrary


@Library ('My-Jenkins-SharedLibrary')_
pipeline {
    agent any 
    
    tools{
        jdk 'jdk11'
        maven 'maven3'
    }
    
    stages{

        stage("build stage"){
            steps{
                script{
                    build() //it will call build.groovy file form My-Jenkins-SharedLibrary
                }
            }
        }
        
        stage("deploy"){
            steps{
                script{
                    deploy()  // it will call deploy.groovy file form My-Jenkins-SharedLibrary
                }
            }
        }
    }
}


# 
