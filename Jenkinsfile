pipeline {
    agent {
        label 'linux' 
    }
    options {
        disableConcurrentBuilds()
    }
    environment {
        WORKSPACE = '/opt/jenkins-workspace/workspace/project-demo'
    }
    stages {
        stage('parallel execution') {
            parallel {
                stage('checkout') {
                    agent {
                        label 'linux'
                    }
                    steps {
                        dir("$WORKSPACE") {
                            echo 'cloning repo'
                            git 'https://github.com/kalyanreddyc/third-demo-ear.git'
                        }
                    }
                }
                stage('build') {
                    agent {
                        label 'linux'
                    }
                    steps {
                        dir("$WORKSPACE") {
                            sh """
                            mvn clean package
                            echo "testing wehboot"
                            """
                        }
                    }
                }
                
            }
        }
        
    }
}
