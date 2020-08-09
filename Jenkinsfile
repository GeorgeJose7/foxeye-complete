pipeline{
  agent any
  
  stages {
    stage ('Checkout'){
      steps{
        dir("customer"){
          sh 'pwd'
          git branch: 'master',
              credentialsId: 'github',
              url: 'https://github.com/GeorgeJose7/customer.git'
        }
        dir("customerLog"){
          sh 'pwd'
          git branch: 'master',
              credentialsId: 'github',
              url: 'https://github.com/GeorgeJose7/customer-log.git' 
        }
        dir("discovery-server"){
          sh 'pwd'
          git branch: 'master',
              credentialsId: 'github',
              url: 'https://github.com/GeorgeJose7/foxeye-discovery.git' 
        }
        dir("frontend"){
          sh 'pwd'
          git branch: 'master',
              credentialsId: 'github',
              url: 'https://github.com/GeorgeJose7/foxeye-frontend.git'
        }
      }
    }
    stage('Build'){
      stages{
        stage('Maven-Builds'){
          steps{
            dir("customer"){
              sh 'mvn clean compile install -DskipTests'
            }
            dir('customerLog'){
              sh 'mvn clean compile install -DskipTests'
            }
            dir('discovery-server'){
              sh 'sh clean compile install -DskipTests'
            }
          }
        }
        stage('Angular-Build'){
          steps{
            sh 'echo running angular build'
          }
        }
      }
    }
    stage('Docker image Build'){
      steps{
        sh 'echo building docker images'
      }
    }
  }
}
