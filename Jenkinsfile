pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Hello World"'
                sh '''
                    mvn package
                '''
                }
                        }
        
        
        stage('push') {
            steps {
                rtUpload  (
    serverId: "jfrog",
    spec:
        """{
          "files": [
            {
              "pattern": "target/*war",
              "target": "java_app"
            }
         ]
        }"""
)
            }
                        }

        
        
            }
    
            }


