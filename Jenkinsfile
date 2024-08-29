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
                echo 'Deployment will be done on my Birthday!!'
            }
        }
        stage('SonarQube analysis') {
            steps {
                withSonarQubeEnv('sonarqube-10.6.0')
                {
                    bat script: """
                    sonar-scanner -D"sonar.projectKey=manya123" \
                    -D"sonar.sources=." \
                    -D"sonar.host.url=http://localhost:9000" \
                    -D"sonar.login=sqa_6bf382a0e813f4497f0e9cedb5854d1dc30a0536"
                    """
                }
            }
        }
    }
}
       


