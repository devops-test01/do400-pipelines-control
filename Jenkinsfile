pipeline {
	agent {
	   node {
             label 'nodejs'
           }
         }
        stages {
            stage('Backend Tests') {
               steps {
                  sh 'node ./backennnnd/test.js'
                }
            }
            stage('Frontend Test') {
               steps {
                  sh 'node -/frontend/test.js'
               }
            }
         }
}
