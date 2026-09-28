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

        stage('Deploy to Staging') {
            steps {
                echo 'Развертывание приложения в staging...'
                echo 'Staging-развертывание выполнено'
            }
        }

        stage('Approval') {
            steps {
                input message: 'Выполнить деплой в Production?',
                      ok: 'Deploy'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Развертывание приложения в Production...'
                echo 'Production-развертывание выполнено'
            }
        }
    }

    post {
        success {
            echo 'CI/CD Pipeline успешно выполнен'
        }

        failure {
            echo 'CI/CD Pipeline завершился с ошибкой'
        }

        always {
            echo 'Работа Pipeline завершена'
        }
    }
}
