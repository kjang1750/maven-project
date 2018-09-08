pipeline {
  agent any
    stages {
      stage('Build') {
        steps {
            sh '''
              mvn -Dmaven.test.failure.ignore=true install
              ls ${WORKSPACE}/target/
        '''
        stash name 'test', includes: "target/*"
          }
      }
    }
}
