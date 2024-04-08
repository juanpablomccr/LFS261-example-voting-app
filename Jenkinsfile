pipeline{
    agent any
    
    stages{
        stage("One"){
            steps{
                echo 'step 1 in testmulti branch'
                sleep 3
            }
        }
        stage("Two"){
            steps{
                echo 'step 2 in testmulti branch'
                sleep 6
            }
        }
        stage("Three"){
            when{
                branch 'master' 
                changeset "**/worker/**"
            }
            steps{
                echo 'step 3 in testmulti branch'
                sleep 5
            }
        }
    }
    post{
        always{
            echo 'This pipeline is completed in testmulti branch'
        }
    }
}
