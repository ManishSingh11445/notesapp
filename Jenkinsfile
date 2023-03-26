pipeline{
agent any
stages {
stage("build docker image"){
steps{
  script {
    sh "docker build -t nodesapp:1.0 ."
  }
}
}
  
  stage("push docker image"){
steps{
  script {
    withCredentials([string(credentialsId: 'dockerhub_cred', variable: 'dockerhub_cred')]) {
      sh "docker login -u manish11445 -p ${dockerhub_cred}"
      sh "docker push nodesapp:1.0"
}
  }
}
}
  
}
}
