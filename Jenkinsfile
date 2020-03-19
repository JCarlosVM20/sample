pipeline {
  agent any
  stages {
    stage('Unit Test') {
      steps {
        sh 'echo "start Minitest"'
        sh label: '', script: '''ruby tests.rb || true 
                                   rm statica.txt'''
            }
      }
      stage('QE') {
        steps {
        sh 'echo "start Rubocop"'
        sh label: '', script: '''cd cidr_convert_api 
                                 rubocop > static.txt || true 
                                 mv static.txt /var/lib/jenkins/workspace/Demo2'''
                  }
        }
    }
}
