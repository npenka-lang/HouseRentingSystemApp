pipeline{
    agent any
    stages{
        stage("Restore dependences"){
            steps{
                bat "dotnet restore"
            }
        }
        stage("Restore build"){
            steps{
                bat "dotnet build --no-restore"
            }
        }
        stage("Run tests"){
            steps{
                bat "dotnet test --no-build --verbosity normal"
            }
        }
    }
}