pipeline {
	agent {
		label 'aj-node'
	}
	stages {
		stage ("Git checkout"){
			steps {
				git branch: "main",
					url: "https://github.com/Research-Associate-Internship/nodejs-goof"
				sh "ls"
			}
		}
		
		stage('Snyk Scan') {
			steps{
				snykSecurity organisation: 'suryaviyyapu', snykInstallation: 'SnykJ', snykTokenId: 'Snyk'
			}
		}				
	}
}
