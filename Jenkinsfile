pipeline {    agent any
    stages {
        stage('clone') {
            steps {
                git clone "https://github.com/phulei/cicd-pipeline-train-schedule-dockerdeploy"
            }
        }
        stage('Build') {
            steps {
                echo 'Running build automation'
                sh './gradlew build --no-daemon'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
    }
 }
}
}
