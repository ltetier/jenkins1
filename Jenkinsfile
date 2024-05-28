pipeline {
    agent any

    stages{
        stage('build'){
            steps{
               echo "hello"
               
            }
        }
    }

    post{
        success{
                emailext(to:'laurenttetier@orange.fr',  body: 'test body', subject: 'test subject')
        }
    }

}