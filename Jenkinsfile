pipeline{
    agent{
        label 'gradle'

    }
    stages{
        stage('Compile'){  
             agent{
                docker {
                    image 'java:8'
                }
             }
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
