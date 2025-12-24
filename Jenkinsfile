pipeline {
    agent any

    stages {
        stage('Deploy on k8s') {
            steps {
                sh 'pwd'
                sh 'cp -R helm/* .'
                sh 'ls -ltr'

                sh '''
                  /usr/local/bin/helm upgrade --install petclinic-app petclinic \
                  --set image.repository=sunnyvalechha/petclinic \
                  --set image.tag=1
                '''
            }
        }
    }
}
