pipeline {
    agent any

    environment {
        PROJECT_NAME = 'jenkins-devops-practice'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Сборка приложения...'
                echo "Проект: ${env.PROJECT_NAME}"
                echo "Номер сборки: ${env.BUILD_NUMBER}"
            }
        }

        stage('Test') {
            steps {
                echo 'Тестирование приложения...'
                echo 'Тестирование успешно завершено'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Развертывание приложения...'
                echo 'Деплой успешно завершен'
            }
        }
    }

    post {
        success {
            echo 'Pipeline успешно выполнен'
        }

        failure {
            echo 'Pipeline завершился с ошибкой'
        }

        always {
            echo 'Работа Pipeline завершена'
        }
    }
}
