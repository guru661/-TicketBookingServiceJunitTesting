pipeline {
    agent any
    stages {
        stage('git repo & clean') {
                bat "git clone https://github.com/kishancs2020/TicketBookingServiceJunitTesting.git"
                bat "mvn clean -f TicketBookingServiceJunitTesting"
            }
        }
        stage('install') {
            steps {
                bat "mvn install -f TicketBookingServiceJunitTesting"
            }
        }
        stage('test') {
            steps {
                bat "mvn test -f TicketBookingServiceJunitTesting"
            }
        }
        stage('package') {
            steps {
                bat "mvn package -f TicketBookingServiceJunitTesting"
            }
        }
    }
}
