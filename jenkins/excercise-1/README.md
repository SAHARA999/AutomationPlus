## Exercise - 1: create a simple pipeline 

1. Login to your Github account with the webbrowser and create a new repository.

2. Create a new repository called jenkins_learning.

3. Check if the student-{x} public sshkey is already added in your repository.

4. Add with the Editor the following content to a file called: jenkinsfile

```
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Production..'
            }
        }
    }
}
```

5. Login to the Jenkins server with your student credentials.

6. Create Jenkins job.

Follow the instuctions.