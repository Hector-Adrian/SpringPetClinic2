pipeline {

    agent any
    tools {maven "mavenV3"}

    stages {
        stage("checkout") {

            steps {
                git branch: "main", url: "https://github.com/Hector-Adrian/SpringPetClinic2"
             }
        }

        stage("build") {
        
            steps {
                sh "mvn compile"
             }
        }

        stage("test") {
            steps {
                sh "mvn test"
            }
        }

        stage("packagew") {
            steps {
                sh "mvn package"
            }
        }

        stage("deploy") {
        
            steps {
                sh "java -jar ./target/*.jar"
            }
        }
    }
}
