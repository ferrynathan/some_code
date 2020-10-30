pipeline {
  agent any
  stages {
    stage('echo') {
      steps {
        echo 'hello from the trigger'
      }
    }

    stage('run it') {
      steps {
        sh '''chmod +x test.sh;
 ./test.sh'''
      }
    }

  }
  triggers {
    cron('H/15 * * * *')
  }
}