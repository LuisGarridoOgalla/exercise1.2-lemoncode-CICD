pipeline{
    agent{
        docker {
            image 'gradle:6.2.2-jdk8'
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
