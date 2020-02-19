pipeline{
    agent any
    stages {
        stage('install'){
            steps {
                
                sh 'gem install bundler'
            }
        
        
        }

        
        stage('build') {
            steps {
                sh 'bundle install'
            }
        }
        stage('docker build')
        {
            steps{
                sh 'docker build -t ankit199112/ankit2:${BUILD_TAG} .'
            }
            
        }
        stage('test'){
            steps {
                sh 'rake'
            }
        }
    }

}
