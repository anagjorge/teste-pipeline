pipeline {
    agent any
    environment {
        BRANCH = 'Master'
    }
    stages {
        stage('step1') {
            steps {
                sh 'printenv'
            }
        }
        stage('step2'){
            steps{
                sh 'printenv'
            }
        }
        stage('step3'){
            when{
                expression { BRANCH ==~ /(Master|Hotfix)/ }
            }
            steps{
                echo "step 3 OK para Master ou Hotfix"
            }
        }
        stage('step4'){
            when{
                expression { BRANCH ==~ /(Release)/ }
            }
            steps{
                echo "step 4 OK para Release"
            }
        }

    }

}
