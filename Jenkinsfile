pipeline {
    agent any

    stages{
        stage('build and test'){
            matrix{
                axes{
                    axis{
                        name 'PLATFORM'
                        values 'linux', 'macos', 'windows'
                    }
                    axis{
                        name 'BROWSER'
                        values 'firefox','chrome','safari'
                    }
                }
                stages{
                    stage('build'){
                        steps{
                            echo "construire pour ${PLATFORM} - ${BROWSER}"
                        }
                    }
                    stage('test'){
                        steps{
                            echo "test pour ${PLATFORM} - ${BROWSER}"
                        }
                    }
                }
            }

        }
        stage('deployment production'){
            steps {
                echo  "deploy !"
            }
        }
    }

}