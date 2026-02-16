pipeline{
    agent any
    stages{
        stage("Build"){
            steps{
               bat "dotnet build"
            }
        }
        stage("Run Test One"){
            steps{
               bat "dotnet test TestProject1/TestProject1.csproj --no-build --verbosity normal"
            }
        }
        stage("Run Test Two"){
            steps{
               bat "dotnet test TestProject2/TestProject2.csproj --no-build --verbosity normal"
            }
        }
        stage("Run Test Three"){
            steps{
               bat "dotnet test TestProject3/TestProject3.csproj --no-build --verbosity normal"
            }
        }
    }
}