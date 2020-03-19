pipeline {
  agent any
  stages {
    stage('Unit Test') {
      steps {
        sh 'echo "start Minitest"'
        sh label: '', script: '''cd cidr_convert_api 
                                 ruby tests.rb > utest.txt || true '''
        //sh 'pwd'
        //sh 'ruby tests.rb || true'
            
            }
      }
      stage('QE') {
        steps {
        //sh 'echo "start Rubocop"'
        //sh 'rubocop > static.txt || true'
        sh 'pwd'
        sh 'ls'
        //sh 'rubocop > static.txt || true'
                  }
        }
    }
}
