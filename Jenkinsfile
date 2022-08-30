
pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
    }
    post {
    success {
        sh 'echo "Pipeline Works"'
    }
    failure {
        script {
            sh '''
            |echo "This job failed"
            |echo "And I am not sure why"
            '''.stripMargin().stripIndent()
        }
    }
}
    

    
}
