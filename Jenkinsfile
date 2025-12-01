pipeline {
    agent any

    tools {
        maven 'Maven 3.8.6'   // Make sure this tool name exists in Jenkins Tools
    }

    stages {
        stage('Checkout') {
            steps {
                echo '🔄 Checking out source code...'
                checkout scm
            }
        }

        stage('Build with Maven') {
            steps {
                echo '🏗️ Building project using Maven...'
                sh 'mvn -B -DskipTests clean package'
            }
        }

        stage('Run Tests') {
            steps {
                echo '🧪 Running Maven tests...'
                sh 'mvn test'
            }
        }
    }
}

