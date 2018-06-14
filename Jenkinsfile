//node {
//    stage ('Stage 1 - scm') {
//        echo 'Stage 1 - scm'
//        sleep 2
//        checkout scm
//    }
//
//    stage ('Stage test') {
//        echo 'test stuff'
//        sh 'touch TEST-*.xml'
//        step([$class: 'JUnitResultArchiver', testResults: 'TEST-*.xml'])
//    }
//
//    stage ('End') {
//        echo 'cheers'
//    }
//
//}

pipeline {
    agent any 
    stages {
        stage('Stage 1 - scm') {
            steps {
                echo 'Stage 1 - scm' 
                sleep 2
                checkout scm
            }
        }
        stage('Stage test') {
            steps {        
                echo 'test stuff'
                sh 'touch TEST-*.xml'
                junit testResults: 'TEST-*.xml'
            }
        }
    }
}
