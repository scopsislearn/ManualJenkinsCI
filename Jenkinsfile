pipeline{
  agent any
  stages {
    stage('build'){
      steps{
        sh 'echo building...'
      }
    }
    stage('Test'){
      steps{
        sh 'python -m unittest'
      }
    }
  }
}
