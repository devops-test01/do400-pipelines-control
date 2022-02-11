pipeline {
	agent {
	   node {
             label 'nodejs'
           }
         }
        stages {
	    stage('Run Test') {
               parallel {

                   stage('Backend Tests') {
                      steps {
                         sh 'node ./backend/test.js'
                      }
                   }
                   stage('Frontend Test') {
                      steps {
                         sh 'node ./frontend/test.js'
                      }
                   }
              }
          }
      }
}
