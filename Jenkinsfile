pipeline {
  agent any
  triggers {
   upstream(upstreamProjects: 'testjob/main', threshold: hudson.model.Result.SUCCESS)
  }
  stages{
    stage('Build') {
      steps{
        sh 'sh ./run_proj1_build.sh'
      }
    }
    stage('Test') {
      steps{
        sh "sh ./run_proj1_test.sh"
      }
    }
  }
}
