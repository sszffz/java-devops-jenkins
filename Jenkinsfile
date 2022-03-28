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
//                 sh "echo ${USER}"
//                 sh "git --version"
                sh "docker version"
//                 sh "mvn -v"
            }
        }

        // 1. compile
        stage('compile') {
//             agent {
//                 docker { image "maven:3-alpine"}
//             }
//             agent {
//                 docker {
//                     image 'maven:3-alpine'
//                 }
//             }
            steps {
                echo "compile ..."
                echo "$hello"
                echo "${world}"
                echo "done compile"
                sh 'pwd && ls -alh'
                sh "mvn -v"
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