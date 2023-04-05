pipeline{
    agent any
    stages{
        stage('1-check engineers name'){
            steps{
                echo "My name is Joyce"
        }
      }  
        stage('2-parallel-jobs first'){
            parallel{
                stage('2-check disk free space in mega byte'){
                    steps{
                       sh 'free -m'
                    }
                }
                stage('3-check disk usage'){
                    steps{
                        sh 'du -h'
                    }
                }
            }
        }
        stage('2-another parallel-jobs second'){
            parallel{
                stage('4-check lscpu'){
                    steps{
                        sh 'lscpu'
                    }
                }
                stage('5-check disk free space in giga byte'){
                    steps{
                      sh 'free -g'
                    }
                }
            }
        }
        stage('6-closing stage'){
            steps{
                echo "team5 group4 techops are done with multibranch Jenkins build jobs"
            }
        }
    }
}