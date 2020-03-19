pipeline {
  agent any
  stages {
    stage('Unit Test') {
      steps {
        //sh 'echo "start Minitest"'
        sh 'pwd'
        sh 'ls'
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
