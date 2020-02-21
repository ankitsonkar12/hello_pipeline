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
        stage('docker push'){
            steps{
                withCredentials([string(credentialsId: 'docker2', variable: 'pswd')]) {
                      
                        sh 'docker login -u ankit199112 -p ${pswd}'
                    }
                    sh 'docker push ankit199112/ankit2:${BUILD_TAG}'
                   
                    

            }
        }
        
    }

}
