node {
    stage 'Provision Slaves'
    sh "echo 'This is the step where the slaves will be provisioned.'"
    build 'Provision Slaves'

    stage 'Run Jobs'
    sh "echo 'This is the step where X number of jobs will run concurrently.'"
    build 'Hello World'

    stage 'Teardown/Idle Slaves'
    sh "echo 'This is the step where the jobs will be checked for complettion.'"
    build 'Teardown or Idle Slaves'
}
