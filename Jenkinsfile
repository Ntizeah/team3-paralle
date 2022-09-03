pipeline{
    agent any
    stages{
        stage('git clone'){
            steps{
                 checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: '301215b5-9b0e-43aa-9ebf-69111a44e065', url: 'https://github.com/Ntizeah/team3-paralle.git']]])
            }
        }
        stage('paralle-leve1'){
            paralle
            stage('sub-job1'){
                steps{
                    echo "sub-job1 task"
                }
            }
            stage('sub job2'){
                steps{
                    echo "sub-job2 task"
                }
            }
        }
    }
    stage('version-check'){
        steps{
            echo "end of paralle job"
        }
    }
}
