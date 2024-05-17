pipeline {
    agent any

    tools{
        gradle 'gradle8.6'
        nodejs 'nodejs22.2'
    }

    stages{
        stage('build'){
            steps{
                sh 'gradle -v'
                sh 'npm -v'
            }
        }
    }

}