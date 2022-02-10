pipeline{
    agent any
    tools{
        jdk 'Java'
        maven 'Mymaven'
    }
    stages{
        stage("COMPILE"){
            steps{
                script{
                    echo "Compiling the code"
                     sh 'mvn compile'
                }
            }
        }
        stage("UNITTEST"){
            steps{
                script{
                    echo "Run the unit test"
                     sh 'mvn test'
                }
            }
        }
        stage("Package"){
            steps{
                script{
                    echo "Building the app"
                    sh 'mvn package'
                }
            }
        }
    }
}       
