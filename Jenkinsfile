pipeline{
    agent any

    environment {
      hello = "adfaf"
      world = "aaaaaaaaaaaaaa"
    }

    stages {
        // 0. environment test
        stage("environment test") {
            steps {
                sh 'printenv'
                sh "echo ${GIT_BRANCH}"
                echo "${GIT_BRANCH}"
                echo "check basic setup ..."
                sh "java -version"
                sh "git --version"
//                 sh "docker version"
                sh "mvn -v"
            }
        }

        // 1. compile
        stage('compile') {
            steps {
                echo "compile ..."
                echo "$hello"
                echo "${world}"
                echo "done compile"
                sh 'pwd && ls -alh'
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