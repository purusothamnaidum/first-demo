pipeline {
       agent any
    //   agent {
     //      label 'test'
      // }

    stages {
    //    stage('checkout') {
      //      steps {
       //         checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/kalyanreddyc/first-demo.git']])
        //    }
        //}
        stage('Print'){
            steps{
        sh '''ls -ltr
        touch test.txt
        mkdir drilldevops'''
            }
        }
    }
}
