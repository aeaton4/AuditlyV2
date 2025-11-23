pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Explicitly specify the 'main' branch
                git branch: 'main', url: 'https://github.com/aeaton4/AuditlyV2.git'
            }
        }
        stage('Deliver Auditly.html') {
            steps {
                // Archive Auditly.html as a Jenkins build artifact
                archiveArtifacts artifacts: 'Auditly.html', fingerprint: true
                // To deploy to a server, add deployment scripts here (e.g., scp or rsync)
            }
        }
    }
}
