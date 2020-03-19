pipeline {
  agent any
  stages {
    stage('QE') {
      steps {
        sh 'echo "checking path"'
        sh 'pwd'
            }
      }
      stage('Unit Test') {
        steps {
        sh 'echo "In progress"'
        sh 'ruby ruby/tests.rb'
              }
        }
    }
}
