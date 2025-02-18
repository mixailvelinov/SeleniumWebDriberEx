pipeline{
    agent any
    stages{
        stage("Checkout the code"){
            steps{
                echo "Checking out the code..."
                git branch: main, url: "https://github.com/mixailvelinov/SeleniumWebDriberEx"
            }
        }

        stage("Setup .NET Core") {
          steps {
            echo "Setting up the .NET Core..."
            bat "choco install dotnet-sdk"
          }
        }

        stage("Restore dependencies") {
          steps {
            echo "Restoring dependencies..."
            bat "dotnet restore"
          }
        }

        stage("Build app") {
          steps {
            echo "Building app..."
            bat "dotnet build"
          }
        }

        stage("Run TestProject1 tests") {
          steps{
            echo "Running TestProject1 tests..."
            bat "dotnet test TestProject1/TestProject1.csproj"
          }
        }

        stage("Run TestProject2 tests") {
          steps{
            echo "Running TestProject2 tests..."
            bat "dotnet test TestProject2/TestProject2.csproj"
          }
        }

        stage("Run TestProject3 tests") {
          steps{
            echo "Running TestProject3 tests..."
            bat "dotnet test TestProject3/TestProject3.csproj"
          }
        }
    }


}
