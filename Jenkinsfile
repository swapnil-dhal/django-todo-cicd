@Library(Shared@main) _
pipeline{
  agent any
  stages{
    stage('Building the image'){
      steps{
        sh ''' pwd
        ls -a
        '''
        sh 'docker build -t python-notes-app .'
      }
      
    }
    stage("Running the app")
    {
      steps{
        echo "in running stage"
        sh 'docker run -d -p 8000:8000 python-notes-app:latest'
      }
    }
  }
}
