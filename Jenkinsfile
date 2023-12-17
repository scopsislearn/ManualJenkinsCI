pipeline{
  agent any
  stages {
    stage('build and test in Docker'){
      steps{
        script{
          docker.image('python:3.8').inside{
            sh 'pip install -r requirements.txt'
            sh 'python -m unittest'
          }
        }
      }
    }
    stage('Post-Merge Action'){
      when {
        branch 'main'
      }
      steps{
        echo 'Any test you desire to do post merge'
      }
    }
  }

  post{
    always{
      echo 'This will alwyas run regardless of the outcome'
    }
    success{
      echo 'Build was Successful!'
    }
    failure{
      echo 'Build Failed!'
    } 
  }
}








    
