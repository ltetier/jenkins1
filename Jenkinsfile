pipeline {
    agent any

    stages{
        stage('Build and Test'){
            steps{
               echo 'Build and Test...'               
            }
        }
        stage('Déploiement en Production'){
            input{
                message "Voulez-vous déployer en production ?"
                ok "Oui, déployons"
                submitter "admin,devops"
                parameters {
                    string(name: 'VERSION', defaultValue: 'latest', description: 'Quelle version souhaitez-vous déployer ?')
                }

            }
            steps{
                echo 'Déploiement de la version ${VERSION} en production'
            }
        }
        stage('Deploy'){
            steps{
                echo 'Etape de déploiement en cours...'
            }
        }
    }

}
