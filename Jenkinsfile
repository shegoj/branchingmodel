pipeline {
  agent any
  stages {
    stage ("code verification") {
      when {
        branch feature*
      }
      steps {
        echo "verifying code done by dev"
        sh 'mvn clean verify'
      }
    }
    stage ("code  install and deploy to dev environment") {
      when {
        branch develop
      }
      steps {
        echo "verifying code done by dev"
        sh 'mvn clean install'
# logic to push to develop
      }
    }
  }
}
