pipeline{
    agent any
    stages{
        stage("Restore dependencies"){
            when{
                branch "main"
            }
            steps{
                 bat 'dotnet restore'
            }
        }
        stage("Build the application"){
            when{
                branch "main"
            }
            steps{
                bat 'dotnet build --no-restore'
            }
        }
        stage("Test the application"){
            when{
                branch "main"
            }
            steps{
                bat 'dotnet test --no-build --verbosity normal'
            }
        }
    }
}