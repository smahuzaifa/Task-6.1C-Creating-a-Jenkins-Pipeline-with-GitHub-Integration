pipeline{
    agent any

    stages{
        stage('Build'){
            steps{
                echo 'Building the code using a build automation tool which will compile and package the code'
                echo 'The tool used is Maven'
            }
        }
        stage('Unit and Integration Testing'){
            steps{
                echo 'Unit testing is done to ensure the code works as per the expectations'
                echo 'Integration testing is also done to ensure multiple components of the applications are working as per the expected behaviour'
                echo 'The tool used for unit testing is JUnit'
                echo 'The tool used for integration testing is Appium'
            }
            post{
                success {
                    mail to: 'huzaifasadath@gmail.com',
                    subject: 'Unit and Integration Testing Status: Success',
                    body: 'The unit and integration testing was done successfully',
                }
                failure{
                    mail to: 'huzaifasadath@gmail.com',
                    subject: 'Unit and Integration Testing Status: Failed',
                    body: 'The unit and integration testing failed. Please check the logs for details',
                }
            }
        }
        stage('Code Analysis'){
            steps{
                echo 'The code is analysed to ensure it is written as per the industry standard'
                echo 'The tool used is SonarQube'
            }
        }
        stage('Security Scan'){
            steps{
                echo 'A security scan is performed to identify any vulnerabilities'
                echo 'The tool used is OWASP ZAP'
            }
            post{
                success {
                    mail to: 'mention email',
                    subject: 'Security scan - SUCCESS',
                    body: 'Security scan was conducted successfully',
                }
                failure{
                    mail to: 'mention email',
                    subject: 'Security scan - FAILED',
                    body: 'Security scan failed',
                }
            }
        }
        stage('Deploy to Staging'){
            steps{
                echo 'The application is being deployed to the staging server'
                echo 'The tool used is Docker with AWS EC2'
            }
        }
        stage('Integration testing on staging'){
            steps{
                echo 'Integration testing is done on the staging environment'
                echo 'The tool used is Postman'
            }
        }
        stage('Deploy to production'){
            steps{
                echo 'The application is being deployed to the production server'
                echo 'The tool used is Kubernetes with AWS EC2'
            }
        }
    }
}
