pipeline {
    agent any
    stages {
        stage("Build") {
            steps {
                bat "dotnet build"
            }
        }

        stage("Run Tests in Parallel") {
            parallel {
                stage("Test Project 1") {
                    steps {
                        bat "dotnet test TestProject1/TestProject1.csproj --no-build --verbosity normal"
                    }
                }
                stage("Test Project 2") {
                    steps {
                        bat "dotnet test TestProject2/TestProject2.csproj --no-build --verbosity normal"
                    }
                }
                stage("Test Project 3") {
                    steps {
                        bat "dotnet test TestProject3/TestProject3.csproj --no-build --verbosity normal"
                    }
                }
            }
        }
    }
}