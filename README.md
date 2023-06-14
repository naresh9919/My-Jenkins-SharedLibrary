# My-Jenkins-SharedLibrary

````
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


# System configuration

Global Pipeline Libraries
Library Name : My-Jenkins-SharedLibrary
Default version : master

Retrieval method

Modern SCM
Source Code Management : Git
Project Repository : https://github.com/naresh9919/My-Jenkins-SharedLibrary.git
Credentials

Filter by name (with wildcards)
Include : master
apply and save

