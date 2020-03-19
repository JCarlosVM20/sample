pipeline {
  agent any
  stages {
    stage('Unit Test') {
      steps {
        //sh 'echo "start Minitest"'
        sh label: '', script: '''cd cidr_convert_api 
                                 ruby tests.rb'''
        //sh 'pwd'
        //sh 'ruby tests.rb || true'
            }
      }
      stage('QE') {
        steps {
        sh 'echo "start Rubocop"'
        sh 'rubocop || true'
              }
        }
    }
}
