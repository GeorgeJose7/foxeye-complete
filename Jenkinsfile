pipeline{
  agent any
  
  stages {
    stage ('Checkout'){
      steps{
        sh 'cd customer'
        git branch: 'master',
            credentialsId: '57a803e6-1985-44a9-9b1d-27d44cf94159',
            url: 'https://github.com/GeorgeJose7/customer.git'
        sh 'cd ..'
      }
    }
  }
}
