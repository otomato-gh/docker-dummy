pipeline {
    agent any

    stages {
        stage ('Clone') {
            steps {
                checkout([
            $class: 'GitSCM',
            branches: scm.branches,
            extensions: scm.extensions + [[$class: 'LocalBranch']],
        ])
            }
        }

        stage ('Git info') {
            steps {
                script {
                    sh 'git fetch && git show-branch'
                }
            }
        }

        
    }
}
