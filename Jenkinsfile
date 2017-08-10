#!/usr/bin/env groovy
node {

    stage ('Provision Slaves') {
        sh "echo 'This is the step where the slaves will be provisioned.'"
        build 'Provision Slaves'
    }

    stage ('Run Jobs') {
        sh "echo 'This is the step where X number of jobs will run concurrently.'"
        // Do jobs in parallel
        parallel firstBranch: {
            build 'Hello World'
        }, secondBranch: {
            build 'Hello World'
        },
        failFast: false // Don't terminate all branches upon the failure in
    }                   // any other branch

    stage ('Teardown/Idle Slaves') {
        sh "echo 'This is the step where the jobs will be checked for complettion.'"
        build 'Tear Down or Idle Slaves'
    }

}

