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
        sh '''chmod +x testscript.sh;
 ./testscript.sh'''
      }
    }

  }
  triggers {
    cron('H/15 * * * *')
  }
}