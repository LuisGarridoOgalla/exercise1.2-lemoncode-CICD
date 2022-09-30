pipeline{
    agent{
        docker{
            image 'gradle:6.6.1-jre8-hotspot'
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
