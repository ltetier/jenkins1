pipeline {
    agent any

    tools{
        gradle 'gradle8.6'
    }

    stages{
        stage('build'){
            steps{
                sh 'gradle -v'
            }
        }
    }

}