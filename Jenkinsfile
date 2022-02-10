
node('nodejs') {
	stage('Checkout') {
		git branch: 'main',
		    url: 'https://github.com/devops-test01/do400-pipelines-control'
	}
	stage('Backend Tests') {
		sh 'node ./backend/test.js'
	}
	stage('Fronted Tests') {
		sh 'node ./frontend/test.js'
	}
}
