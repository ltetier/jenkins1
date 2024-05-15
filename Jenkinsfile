pipeline {
    agent any

    parameters {
        booleanParam(name: 'DEPLOY_TO', defaultValue: false, description: 'deploy to prod ?')
    }

    stages{
        stage('build'){
            steps {
                echo  "build !"
            }
        }

        stage('deployment production'){
            when{
                allOf{
                    branch 'master'
                    equals expected: true, actual: params.DEPLOY_TO
                }
            }
            steps {
                echo  "deploy !"
            }
        }
    }

}