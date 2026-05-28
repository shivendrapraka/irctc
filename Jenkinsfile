pipeline {
    agent any

    environment {
        PATH = "/opt/maven/bin:${env.PATH}"
    }

    stages {

        stage("git clone") {
            steps {
                git url: 'https://github.com/shivendrapraka/irctc.git', branch: 'main'
            }
        }

        stage("build") {
            steps {
                sh 'mvn clean install'
            }
        }
    }
}
