pipeline {
	agent {
		label 'docker-node'
	}
	environment {
        SNYK_TOKEN = credentials('snykajtoken')
    }
	stages {
		stage ("Git checkout"){
			steps {
				git branch: "main",
					url: "https://github.com/Research-Associate-Internship/nodejs-goof"
				sh "ls"
			}
		}
		
		//stage('Snyk Scan') {
		//	steps{
		//		snykSecurity failOnIssues: false, organisation: 'abhishekjosyula1122', snykInstallation: 'SnykJ', snykTokenId: 'Snyk'
		//	}
		//}				
	}
}
