pipeline {
    agent { label 'master'}
    stages {
        stage('git checkout'){
            steps{
                script{
                    git credentialId: 'git', url: 'https://github.com/'
           }
          }
        }
        stage('maven compile'){
            steps{
                script{
                    withMaven(jdk : 'jdk8', maven : 'maven'){
			sh 'mvn clean install'
           }
          }
         }
        }
    }
}
