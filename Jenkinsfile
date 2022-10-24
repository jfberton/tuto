pipeline {
    agent { label 'tuto' }
    

    stages {
        stage('Build') {
            steps {
                container('podman') {
                    script {
                        sh 'podman run hello-world'
                    }
                }
                container('kubectl') {
                    script {
                        sh 'env'
                        sh 'kubectl get pods --all-namespaces'
                    }
                }
                container('fortune'){
                    script{
                        sh 'fortune'
                    }
                }
            }
        }
    }
}
