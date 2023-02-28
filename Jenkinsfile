pipeline {
    agent any

    stages {
        stage('Installing SnowSQL') {
            steps {
                script {
                    sh '''
                    wget https://sfc-repo.snowflakecomputing.com/snowsql/bootstrap/1.2/linux_x86_64/snowsql-1.2.24-linux_x86_64.bash
                    chmod +x snowsql-1.2.24-linux_x86_64.bash
                    printf "/usr/bin/\ny" | bash snowsql-1.2.24-linux_x86_64.bash
                    snowsql
                    '''
                }
            }
        }
    }
}