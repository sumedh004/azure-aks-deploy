pipeline {
    agent any
    stages {
        stage('Deploy aks') {
            steps {
                script {
                    withKubeConfig([credentialsId: 'kubeconfig']) {
                        sh 'kubectl apply -f deploy.yml'                        
                    }
                }                               
            }
        }
    }
}
