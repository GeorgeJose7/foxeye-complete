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
        dir("api-gateway"){
          sh 'pwd'
          git branch: 'master',
              credentialsId: 'github',
              url: 'https://github.com/GeorgeJose7/foxeye-gateway.git'
        }
        dir("config-server"){
          sh 'pwd'
          git branch: 'master',
              credentialsId: 'github',
              url: 'https://github.com/GeorgeJose7/foxeye-config-server.git'
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
              sh 'mvn clean compile install -DskipTests'
            }
            dir('api-gateway'){
              sh 'mvn clean compile install -DskipTests'
            }
            dir('config-server'){
              sh 'mvn clean compile install -DskipTests'
            }
          }
        }
        stage('Angular-Build'){
          steps{
            dir('frontend'){
              sh 'npm update'
              sh 'ng build --prod'
            }
          }
        }
      }
    }
    stage('Docker image Build'){
      steps{
        sh 'rm docker-compose-local.yml'
        sh 'sudo docker-compose up'

      }
    }
  }
}
