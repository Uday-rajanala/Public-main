pipeline {
    agent (node1)
    stages {
        stage('Install Dependencies') {
            steps {
                sh '''
                    python3 -m venv venv
                    . venv/bin/activate
                    pip install --upgrade pip
                    pip install -r requirements.txt
                '''
            }
        }
        stage('Run App') {
            steps {
                sh '''
                    . venv/bin/activate
                    python app.py
                '''
            }
        }
    }
}
