#!/usr/bin/env groovy

pipeline {
    agent any
    stages {
        stage ('Run Jobs, first batch') {
            sh "echo 'This is the step where X number of jobs will run concurrently, first batch.'"
            // Do jobs in parallel
            parallel firstBranch: {
                sh "echo 'Hello World! First'"
            }, secondBranch: {
                sh "echo 'Hello World! Second'"
            },
            failFast: false // Don't terminate all branches upon the failure in
        }                   // any other branch

        stage ('Run Jobs, second batch') {
            sh "echo 'This is where the second batch will run.'"
        }
    }
}
