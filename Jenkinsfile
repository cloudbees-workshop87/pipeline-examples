import javaposse.jobdsl.dsl.DslFactory

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
                pipelineJob()

            } }
} }

def pipelineJob() {
 
    definition {
        cpsScm {
            scm {
                github('cloudbees-workshop87/pipeline-examples')
            }
            scriptPath('declarative-examples/simple-examples/environmentInStage.groovy')
        }
    }
}
