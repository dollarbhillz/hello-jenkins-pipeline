#!/usr/bin/env groovy
node {

    stage ('Provision Slaves') {
        sh "echo 'This is the step where the slaves will be provisioned.'"
        build 'Provision Slaves'
        sh "su -c 'yum install -y atomic-origin-clients'"
    }

    stage ('Run Jobs') {
        sh "echo 'This is the step where X number of jobs will run concurrently.'"
        build 'Hello World'
    }

    stage ('Teardown/Idle Slaves') {
        sh "echo 'This is the step where the jobs will be checked for complettion.'"
        build 'Tear Down or Idle Slaves'
    }

}

