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
            sh 'docker build -t ankit199112/ankit:${buildnumber} .'
        }
        stage('test'){
            steps {
                sh 'rake'
            }
        }
    }

}
