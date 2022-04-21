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
                git {
                    remote {
                        url(https://github.com/cloudbees-workshop87/pipeline-examples.git)
                    }
                }
            }
            scriptPath('declarative-examples/simple-examples/environmentInStage.groovy')
        }
    }
}
            } }
} }
