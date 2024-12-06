pipeline {
    agent {
        label 'workstation'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Build'
            }
        }

        stage('Unit Test') {
            steps {
                echo 'Unit Test'
                // Uncomment the following lines as per your project requirements
                // sh 'npm test'
                // sh 'python -m unittest'
                // sh 'mvn test'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'sonar'
                sh 'sonar-scanner -Dsonar.host.url=http://sonarqube_private_ip:9000 -Dsonar.login=admin -Dsonar.password=admin123 -Dsonar.projectkey=cart'
            }
        }

        stage('Security Checks') {
            steps {
                echo 'Security Checks'
            }
        }

        stage('Publish an Artifact') {
            when {
                expression {
                    env.TAG_NAME ==~ ".*"
                }
            }
            steps {
                echo 'Publish an Artifact'
            }
        }
    }
}
