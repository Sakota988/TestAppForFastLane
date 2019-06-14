pipeline {
    //fastlane requires some environment variables set up to run correctly. In particular, having your locale not set to a UTF-8 locale will cause issues with building and uploading your build. In your shell profile add the following lines:
    environment{
        LC_ALL='en_US.UTF-8'
        LANG='en_US.UTF-8'
    }
    // if process lasts more than 1 hour, than abort process
    options {
        timeout(time: 1, unit: 'HOURS')
    }

    //The agent section specifies where the entire Pipeline, or a specific stage, will execute in the Jenkins environment depending on where the agent section is placed. The section must be defined at the top-level inside the pipeline block, but stage-level usage is optional.
    agent any
    stages {
	
        stage('Build') {
            steps {
                sh('fastlane build')
            }
        }
        
    }
 
}
