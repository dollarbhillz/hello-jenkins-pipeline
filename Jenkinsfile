#!/usr/bin/env groovy
node {

    stage ('Provision Slaves') {
        steps {

            sh "echo 'This is the step where the slaves will be provisioned.'"
            build 'Provision Slaves'
            sh "yum install -y atomic-origin-clients"
        }
    }

    stage ('Run Jobs') {
        steps {
            sh "echo 'This is the step where X number of jobs will run concurrently.'"
            build 'Hello World'
        }
    }

    stage ('Teardown/Idle Slaves') {
        steps {
            sh "echo 'This is the step where the jobs will be checked for complettion.'"
            build 'Tear Down or Idle Slaves'
        }
    }

}

