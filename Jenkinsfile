pipeline {
  agent any
//   triggers { 
//     upstream(upstreamProjects: "../testjob/master", threshold: hudson.model.Result.SUCCESS) 
//   }
//   triggers {
//     upstream("testjob", threshold: hudson.model.Result.SUCCESS)
//   }
//   triggers {
//     upstream('testjob', thresholdhudson.model.Result.SUCCESS)
//   }
  triggers {
  upstream 'testjob'
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
