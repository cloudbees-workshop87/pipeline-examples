pipeline {
    
    agent any

    stages {
        stage('Example') {
            steps {
                echo 'sending helloWorld'
                publishEvent simpleEvent('helloWorld')
            }
        }
   

        stage('Deploy'){
            steps{
pipelineJob('CD_VIEW') {
 
    definition {
        cpsScm {
            scm {
                github('cloudbees-workshop87/pipeline-examples')
            }
            scriptPath('declarative-examples/simple-examples/environmentInStage.groovy')
        }
    }
}
            } }
} }
