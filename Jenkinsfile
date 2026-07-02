pipeline {

    agent any

    stages {

        stage('Diagnostico') {

            steps {

                bat 'whoami'
                bat 'dir "C:\\Users\\DAVID ELEZ\\AppData\\Roaming\\npm"'

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
