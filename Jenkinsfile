pipeline{
  agent any
  stages {
     stage('clone Repo')
           {
	  steps{
               git clone 'https://github.com/Patil-Satyajeet/devops-jenkins-ansible.git'
               }
           }
     stage('ansible dryn run')
          {
         steps{
              sh 'ansible-playbook deploy.yml --check'
              }
          }
     stage('ansible-apply')
         {
        steps{
             sh 'ansible-playbook deploy.yml'
             }
         }
        }
