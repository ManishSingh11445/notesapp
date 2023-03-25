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

}
}
