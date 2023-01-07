pipeline {
    agent any
    parameters{
        string (name: 'person', defaultValue: 'vipin kumar',description: "who are you")
        booleanParam (name: "is male", defaultValue: true, description: "gender")
        
    }
    

    stages {
        stage('Run a command') {
            steps {
                sh 'date'
                sh 'pwd'
            }
        }
        stage('Envirnment variable') {
            steps {
                sh 'echo "${BUILD_ID}"'
            }
        }
        stage('parameters') {
            steps {
                echo 'print perameters'
                sh 'echo "${name}"'
            }
        }
        stage('continue?') {
            input{
                message "should we continue?"
                ok "yes we should"
            }  
            steps {
                echo "parameterised"
            }
        }
    }
}
