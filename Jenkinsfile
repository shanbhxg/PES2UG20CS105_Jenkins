pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo '---'
                echo 'Build Stage Started'
                sh 'g++ -o pes2ug20cs105.exe hello.cpp'
                echo 'Build Stage Completed'
                echo '---'
            }
        }
        stage('Test') {
            steps {
                echo '---'
                echo 'Test Stage Started'
                sh './pes2ug20cs105.exe'
                echo 'Test Stage Completed'
                echo '---'
            }
        }
        stage('Deploy') {
            steps {
                echo '---'
                echo 'Deploy Stage Started'
                sh 'echo "Deploy to Production"'
                echo 'Deploy Stage Completed'
                echo '---'
            }
        }
    }
  post {
    failure {
        echo '---'
        echo 'Build Failed'
        echo '---'
    }
  }
}
