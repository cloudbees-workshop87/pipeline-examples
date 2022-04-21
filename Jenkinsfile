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
    def repo = 'https://github.com/cloudbees-workshop87/pipeline-examples.git'
    definition {
        cpsScm {
            scm {
                git {
                    remote {
                        url(repo)
                    }
                }
            }
            scriptPath('declarative-examples/simple-examples/environmentInStage.groovy')
        }
    }
}
            } }
} }
