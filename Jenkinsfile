

pipeline {
    agent any
    stages {
        parameters{
            choice(name: 'VERSION', choices: ['1.1.0', '1.2.0', '1.3.0'], description: '')
            booleanParam(name: 'executeTests', defaultValue: true, description: '')

        }
       
        stage("build") {
            steps {
                echo 'building the application ...'
                
            }
        }
        stage("test") {
            when{
                expression{
                    params.executeTests
                }
            }
            steps {
                echo 'testing the application ...'
            }
        }
        stage("deploy") {
            steps {
                echo 'deploying the application... '
                echo 'deploying version ${params.VERSION}'
                
            }
        }
    }
}
