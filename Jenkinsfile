pipeline {
    agent any

    environment {
        SONAR_TOKEN = credentials('sonar-token')
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/syedifteqar1/codtech-task4.git'
            }
        }
// stage('OWASP ZAP Scan') {
//     steps {
//         sh '''
//         docker run --rm owasp/zap2docker-stable \
//         zap-baseline.py \
//         -t http://localhost \
//         -r zap_report.html
//         '''
//     }
// }

// stage('Archive Report') {
//     steps {
//         archiveArtifacts 'zap_report.html'
//     }
// }

pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('SonarQube Analysis') {
            steps {
                withSonarQubeEnv('SonarQube') {
                    sh '''
                    sonar-scanner \
                    -Dsonar.projectKey=codtech-task4 \
                    -Dsonar.projectName="CODTECH Task 4" \
                    -Dsonar.sources=.
                    '''
                }
            }
        }
    }
}
