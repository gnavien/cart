pipeline {
    agent{
        node { label 'workstation'}
    }

    stages {

    stage('Code Checkout') {
        steps{
            echo 'Code Checkout'
        }
    }
    stage('Build') {
            steps{
                echo 'Build'
            }
    }

    stage(' Unit Test') {
            steps{
                echo 'Unit Test'
            }
    }
    stage('Code Analysis') {
            steps{
                echo 'Code Analysis'
            }

    }
    stage('Security Checks') {
            steps{
                echo 'Security Checks'
            }
    }
    stage('Publish a Artifact ') {
            steps{
                echo 'Publish a Artifact'
            }
    }
}