pipeline{
    agent any

    environment {
      hello = "adfaf"
      world = "aaaaaaaaaaaaaa"
    }

    stages {
        // 1. compile
        stage('compile') {
            steps {
                echo "compile ..."
                echo "$hello"
                echo "${world}"
                echo "done compile"
            }
        }

        // 2. test
        stage('test') {
            steps {
                echo "test ..."
            }
        }

        // 3. pack
        stage('pack') {
            steps {
                echo "pack ..."
            }
        }

        // 4. deploy
        stage('deploy') {
            steps {
                echo "deploy ..."
            }
        }
    }
}