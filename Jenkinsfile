node {
    stage("Checking out") {
        checkout scm
    }

    stage('Unit testing') {
        withMaven(maven: 'maven'){
            sh 'mvn test'
        }
    }

    stage("Deploying to artifactory") {
        withMaven(maven: 'maven'){
            sh 'mvn clean deploy:deploy'
        }
    }
}