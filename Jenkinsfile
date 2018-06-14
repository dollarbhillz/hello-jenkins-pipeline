#!/bin/env groovy

pipeline {
    agent { node { label 'jenkins-slave' } }
    stages {
        stage ('Install dependencies') {
            steps {
                sh "echo 'Install necessary packages'"
                sh "yum repolist > /dev/null && yum install -y python-setuptools python-psutil python-flask python-pip"
                // Do jobs in parallel
                //parallel firstBranch: {
               //    sh "echo 'Hello World! First'"
                //}, secondBranch: {
                 //    sh "echo 'Hello World! Second'"
                //},
                //failFast: false // Don't terminate all branches upon the failure in
                       // any other branch
            }
        }

        stage ('Run Job') {
            steps {
                sh "echo 'Run pip --version'"
                sh "pip --version"
                sh "echo 'Dev branch'"
            }
        }
    }
}
