pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the code...'
                echo "Using a build automation tool like Maven" 
                echo "mvn clean package"
                echo "Build completed"
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Running Unit and Integration tests...'
                echo "Using test automation tools like JUnit or TestNG for unit tests" 
                echo "mvn test"
            }
            post {
                always {
                    mail to: "joypatel24102001@gmail.com",
                    subject: "Unit and Integration Tests Success Notification", 
                    body: "Unit and Integration tests completed"
                }
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Running code analysis...'
                echo "Using a code analysis tool like SonarQube"
                echo "Installing and configuring SonarQube Scanner in Jenkins" 
                echo "sonar-scanner"
                echo "Code Analysis completed"
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Performing security scan...'
                echo "Using Snyk for security vulnerability scanning" 
                echo "Security scanning completed"
            }
            post {
                always {
                    mail to: "joypatel24102001@gmail.com",
                    subject: "Security Scan Success Notification", 
                    body: "Security Scannning completed"
                }
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to staging environment...'
                echo "Deploying to staging environement AWS EC2"
                echo "Deployment to staging environment completed"
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo "Running integration tests on the staging environment..." 
                echo "mvn integration-test"
                echo "Inetgration tests on Staging completed"
            }
            post {
                always {
                    mail to: "joypatel24102001@gmail.com",
                    subject: "Integration Tests on Staging Success Notification", 
                    body: "Integration tests on staging completed"
                }
            }
        }
        stage('Deploy to Production') {
            steps {
                echo "Using a deployment tool or script to deploy to production server"
                echo 'Deploying to production environment AWS EC2...'
                echo "Deployment to Production completed"
            }
        }
    }
}
