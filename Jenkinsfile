node {
    stage ('Stage 1 - scm') {
        echo 'Stage 1 - scm' 
        sleep 2
        checkout scm
    }
    
    stage ('Stage test') {
        echo 'test stuff'
        sh 'touch TEST-*.xml'
        step([$class: 'JUnitResultArchiver', testResults: 'TEST-*.xml'])
    }
    
    stage ('End') {
        echo 'cheers'
    }    
    
}
