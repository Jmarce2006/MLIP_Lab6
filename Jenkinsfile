pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh '''#!/bin/bash
                echo 'In C or Java, we can compile our program in this step'
                echo 'In Python, we can build our package here or skip this step'
                '''
            }
        }
        stage('Test') {
            steps {
                sh '''#!/bin/bash
                echo 'Test Step: We run testing tool like pytest here'

                # Source the conda init script
                # source /opt/conda/etc/profile.d/conda.sh

                # Activate the conda environment
                #conda activate mlip

                # Run the tests
                /opt/conda/bin/conda run -n mlip pytest

                echo 'Pytest finished'
                '''
            }
        }

        stage('Deploy') {
            steps {
                echo 'In this step, we deploy our porject'
                echo 'Depending on the context, we may publish the project artifact or upload pickle files'
            }
        }
    }
}
