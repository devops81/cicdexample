pipeline {
  agent any
  stages {
    stage('Fluffy Build') {
      steps {
        echo 'Fluffy stage'
        sh 'echo Another placeholder'
      }
    }

    stage('Fluffy Test') {
      steps {
        echo 'Fluffy Test'
        sh 'sleep 5'
        sh 'echo success !!'
      }
    }

    stage('Fluffy Deploy') {
      steps {
        echo 'Fluffy Deploy'
        archiveArtifacts(artifacts: 'feed-combiner-java8-webapp/target/*.war', fingerprint: true, onlyIfSuccessful: true)
      }
    }

  }
}