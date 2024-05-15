pipeline {
    agent any

    parameters{
        string(name: 'NAME', defaultValue: 'M. Jenkins', description: 'Qui est-ce?')
        text(name: 'TEXT', defaultValue: 'un text', description: 'une description')
        booleanParam(name: 'TOGGLE', defaultValue: 'true', description: 'true or false')
        choice(name: 'CHOICE', choices: ['un', 'deux', 'trois'], description: 'liste')
        password(name: 'PASSWORD', description: 'un mot de passe')
    }

    stages{
        stage('build'){
            steps {
                echo  "NAME: ${ NAME }"
                echo  "TEXT: ${ TEXT }"
                echo  "TOGGLE: ${ TOGGLE }"
                echo  "CHOICE: ${ CHOICE }"
                echo  "PASSWORD: ${ PASSWORD }"
            }
        }
    }

}