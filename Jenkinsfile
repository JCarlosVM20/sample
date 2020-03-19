pipeline {
  agent any
  stages {
    stage('Unit Test') {
      steps {
        sh 'echo "start Minitest"'
        sh label: '', script: '''cd cidr_convert_api 
                                   ruby tests.rb > utest.txt || true 
                                   mv utest.txt /var/lib/jenkins/workspace/Demo2'''
            }
      }
      stage('QE') {
        steps {
        sh 'echo "start Rubocop"'
        sh label: '', script: '''cd cidr_convert_api 
                                 rubocop > statica.txt || true 
                                 mv statica.txt /var/lib/jenkins/workspace/Demo2'''
                  }
        }
    }
}
