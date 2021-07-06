pipeline {
    agent any
    stages {
        stage ('Compile') {
            steps {
                withMaven {
                    sh 'mvn clean compile'
                }
            }
        }
        stage ('Unit Test') {
            steps {
                withMaven {
                    sh 'mvn test'
                }
            }
        }
        stage ('Sonar') {
            steps {
                withMaven {
                    sh 'mvn sonar:sonar'
                }
            }
        }
        stage ('Install') {
            steps {
                withMaven {
                    sh 'mvn install'
                }
            }
        }
        stage ('Build') {
            steps {
                withMaven {
                    sh 'mvn package'
                }
            }
        }

    }
}
