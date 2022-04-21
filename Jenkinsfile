pipeline {
    agent any

    stages {
        stage('Example') {
            steps {
                echo 'sending helloWorld'
                publishEvent simpleEvent('helloWorld')
            }
        }
    }
}

pipelineJob('CD_VIEW') {
    definition {
        cpsScm {
            scm {
                git {
                    remote {
                        github('jenkinsci/pipeline-examples')
                    }
                }
            }
            scriptPath('declarative-examples/simple-examples/environmentInStage.groovy')
        }
    }
}
