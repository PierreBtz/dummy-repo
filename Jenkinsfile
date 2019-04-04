pipeline {
    agent any
    stages {
    	stage('Example Glob') {
            when { changeset '**/*test*/**' }
            steps {
                echo 'Test file contained in the changeset'
                attachBranch()
            }
        }
    }
}

def attachBranch() {
    def branchName = env.BRANCH_NAME.trim()
    if (branchName in ['master', 'develop']) {
        sh "git checkout ${branchName}"
        echo "attached the checkout to ${branchName}"
    } else {
        echo 'skipped branch attachment'
    }
}
