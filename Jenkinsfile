pipeline{
    agent any

    stages{
        stage("Restore dependencies"){
            steps{
                bat 'dotnet restore'
            }
            post{
                always{
                    echo "Success!"
                }
            }
        }
        stage("Build solutions"){
            steps{
                bat 'donet build'
            }
        }
        stage("Run tests"){
            steps{
                bat 'dotnet test'
            }
        }
    }
    post{
        always{
            echo "Workflow completed successfully!"
        }
    }
}