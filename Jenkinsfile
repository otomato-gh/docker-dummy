pipeline {
    agent any

    stages {
            steps {
              checkout scm
            }
        }

        stage ('Git info') {
            steps {
                script {
                    sh '''
                        git show-branch | grep '*' | grep -v "$(git rev-parse --abbrev-ref HEAD)" | head -n1 | sed "s/.*\\[\\(.*\\)\\].*/\\1/" | sed "s/[\\^~].*//"
                    '''
                    echo "more testing"
                }
            }
        }

        
}

