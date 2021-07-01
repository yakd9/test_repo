<<<<<<< HEAD
def gv

pipeline {
    agent any
    parameters {
        choice(name: 'VERSION', choices: ['1.1.0', '1.2.0', '1.3.0'], description: '')
        booleanParam(name: 'executeTests', defaultValue: true, description: '')
    }
    stages {
        stage("init") {
            steps {
                script {
                   gv = load "script.groovy" 
                }
            }
        }
        stage("build") {
            steps {
                script {
                    gv.buildApp()
                }
            }
        }
        stage("test") {
            when {
                expression {
                    params.executeTests
                }
            }
            steps {
                script {
                    gv.testApp()
                }
            }
        }
        stage("deploy") {
            steps {
                script {
                    gv.deployApp()
                }
            }
        }
    }   
}
=======
pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
               echo "build start"
            }
        }
        stage('Test') { 
            steps {
                echo "  test start"
        }
        stage('Deploy') { 
            steps {
                 echo "Deploy start"
            }
        }
    }
}
>>>>>>> 9d2eebd03749a47e3be03262e52fa897dcdc8c75
