pipeline{
    agent none
    tools{
        jdk 'Java'
        maven 'Mymaven'
    }
    stages{
        stage("COMPILE"){
            agent {label 'linux_slave'}
            steps{
                script{
                    echo "Compiling the code"
                     sh 'mvn compile'
                }
            }
        }
        stage("UNITTEST"){
            agent any
            steps{
                script{
                    echo "Run the unit test"
                     sh 'mvn test'
                }
            }
        }
        stage("Package"){
            agent {label 'linux_slave'}
            steps{
                script{
                    echo "Building the app"
                    sh 'mvn package'
                }
            }
        }
    }
}       
