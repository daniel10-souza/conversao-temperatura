pipeline { 
    agent any 
 
    stages { 

        stage('Deploy Kubernetes') { /* quarta etapa */
            agent { 
                kubernetes {
                    cloud 'kubernetes' 
                }
            }
            environment{
                tag_version = "${env.BUILD_ID}" 
            }
            steps {
                script {
                    kubernetesDeploy(configs: '**/src/**', kubeconfigId: 'kubeconfig') 
                }
            }
        }
    }
}
    