pipeline{
    agent{
        docker{
            image 'lemoncode/jenkins'
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
