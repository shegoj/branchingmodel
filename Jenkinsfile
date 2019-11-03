pipeline {
  agent any
  stages {
    stage ("code verification") {
      when {
        branch 'featurea/1.0'
      }
      steps {
        echo "verifying code done by dev"
        sh 'mvn clean verify'
      }
    }
    stage ("code  install and deploy to dev environment") {
      when {
        branch 'develop'
      }
      steps {
        echo "verifying code done by dev"
        sh 'mvn clean install'
      }
    }
  }
}
