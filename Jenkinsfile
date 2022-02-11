pipeline {
	agent {
	   node {
             label 'nodejs'
           }
         }
        parameters {
            booleanParam(name: "RUN_FRONTEND_TESTS", defaultValue: true)
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
                      when { expression { params.RUN_FRONTEND_TESTS } }
                      steps {
                         sh 'node ./frontend/test.js'
                      }
                   }
                }
             }
             stage('Deploy') {
                when {
                  expresion { env-GIT_BRANCH == 'origin/main' }
                }
                steps {
                  echo 'Deploying...'
                }   
             }   
        }
} 
