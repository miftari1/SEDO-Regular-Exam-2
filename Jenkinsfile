pipeline {
    agent any
  
    stage('Restore dependencies') {
        steps {
            bat 'dotnet restore'
        }
    }

    stage('Build app') {
        steps {
            bat 'dotnet build --no-restore'
        }
    }

    stage('Run tests') {
        steps {
            bat 'dotnet test --no-build --verbosity normal'
        }
    }
