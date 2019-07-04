pipeline {
    agent { label 'master'}
    stages {
        stage('git checkout'){
            steps{
                script{
                    git branch: '$branch', credentialsId: '21cec4b1-d14d-41b5-9550-d861c8c59d79', url: 'https://github.com/harisareddy/Jenkins.git'
           }
          }
        }
        stage('shell execution'){
            steps{
                script{
			sh '''
			cd /var/lib/jenkins/jobs/Jenkins_workshop/workspace/
			mkdir -p test_parameter
			touch test1
			'''
           }
          }
        }
    }
}
