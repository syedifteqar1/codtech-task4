pipeline {
    agent any

    environment {
        SONAR_TOKEN = credentials('sonar-token')
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/syedifteqar1/codtech-task4.git'
            }
        }

        stage('SonarQube Scan') {
            steps {
                sh 'sonar-scanner -Dsonar.projectKey=codtech-task4 -Dsonar.sources=. -Dsonar.host.url=http://localhost:9000 -Dsonar.login=$SONAR_TOKEN'
            }
        }

        // You can comment out OWASP ZAP stage for now
        // stage('OWASP ZAP Scan') {
        //     steps {
        //         sh 'docker run --rm owasp/zap2docker-stable zap-baseline.py -t http://localhost -r zap_report.html'
        //     }
        // }

        // stage('Archive Report') {
        //     steps {
        //         archiveArtifacts 'zap_report.html'
        //     }
        // }
    } // end stages
} // end pipeline

