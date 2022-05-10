pipeline {
    agent any

    stages {
        stage ('Clone') {
            steps {
                script{
                    cleanWs()
                }
              checkout scm
            }
        }

        stage ('Git info') {
            steps {
                script {
                    sh '''
                        echo child
                        PARENT=`git log --pretty=oneline --decorate | grep 'origin/heads' | grep -v HEAD | head -n1 |  sed "s/.*origin\\/heads\\/\\(.*\\)) .*/\\1/"`
                        echo PARENT is $PARENT
                    '''
                    echo "more testing"
                }
            }
        }
}
        
}

