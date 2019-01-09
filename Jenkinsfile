pipeline {
    agent any
    stages {
    	stage('Example Glob') {
            when { changeset '**/*test*/**' }
            steps {
                echo 'Test file contained in the changeset'
            }
        }
    }
}

