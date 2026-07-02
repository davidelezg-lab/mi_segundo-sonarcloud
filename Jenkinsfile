pipeline {

    agent any

    stages {

        stage('Diagnostico') {

            steps {

                bat 'whoami'
                bat 'where sonar-scanner'
                bat 'echo %PATH%'

            }

        }

        stage('Compilar') {

            steps {

                bat 'g++ main.cpp -o app.exe'

            }

        }

        stage('Analisis SonarCloud') {

            steps {

                withSonarQubeEnv('SonarCloud') {

                    bat '"C:\\Users\\DAVID ELEZ\\AppData\\Roaming\\npm\\sonar-scanner.cmd"'

                }

            }

        }

    }

}

