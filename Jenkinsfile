pipeline {
    agent any

    triggers{
        pollSCM('* * * * *')
    }

    stages{
        stage('build'){
            steps {
                echo  "build !"
            }
        }

        stage('deployment production'){
            input{
                message 'Voulez-vous déployer en production?'
                ok 'Déployer !'
                submitter 'admin,devops'
                submitterParameter 'USER_SUBMIT'
                parameters{
                    string(name: "VERSION", defaultValue: 'latest', description: 'la version déployée')
                }
            }
            steps {
                echo "USER: ${ USER_SUBMIT }"
                echo "version: ${ VERSION }"
                echo  "deploy !"
            }
        }
    }

}