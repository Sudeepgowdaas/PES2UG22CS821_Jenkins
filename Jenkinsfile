pipeline {
    agent any

    stages {
    //    stage('Clone repository') {
     //       steps {
   //           check([$class: 'GitSCM',
       //              branches: [[name: '*/main']],
        //             userRemoteConfigs: 'g++ -o your_executable_name your_cpp_file.cpp'
         //   }
      //  }
        stage('Build') {
            steps {
                build 'PES2UG22CS821-1'
                sh 'g++ main.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }

    post {
        failure {
            error 'Pipeline failed.'
        }
    }
}
