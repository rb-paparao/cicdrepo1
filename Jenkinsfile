pipeline {
  agent any
  stages {
    stage('Satge1') {
      steps {
        sh '''gcloud auth configure-docker us-west1-docker.pkg.dev 
 gcloud auth print-access-token|sudo docker login -u oauth2accesstoken --password-stdin https://us-west1-docker.pkg.dev
 sudo docker build -t us-west1-docker.pkg.dev/dnblab1/garlabrepo1/jenapp1:mynginx .
 sudo docker push us-west1-docker.pkg.dev/dnblab1/garlabrepo1/jenapp1:mynginx'''
      }
    }

    stage('stage2') {
      steps {
        sh 'echo "execution Completed"'
      }
    }

  }
}