pipeline{
    stages{
        stage('Checkout'){
            steps{
                git branch: "${GIT_BRANCH}"
                    url: "${GIT_URL}"
            }
        }
        stage('Install Dependencies') {
            steps {
                script{
                    pip install -r requirements.txt
                }
            }
        }
        stage('Run'){
            steps{
                script{
                    python3 main.py
                }
            }
        }
    }
}