pipeline{
    agent{
        docker {
            image 'openjdk:11'
            args  '-v /tmp:/tmp'
            reuseNode true
        }

    }
    stages{
        stage('Compile'){   
            steps{
                
             sh '''
                chmod +x gradlew
                gradle wrapper
                ./gradlew compileJava'''
            }
        }
        stage('Unit Test'){
            steps{

                sh '''
                chmod +x gradlew
                ./gradlew test
                '''
            }
        }
    
    }
}
