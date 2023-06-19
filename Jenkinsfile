def compile() {
    sh '''
        ./mvnw clean install -DskipTests
    '''
    sleep 5
}
def refreshDB() {
    echo 'I am refreshing db'
    sleep 10
}

node('master'){
    properties([parameters([
        string(defaultValue: 'master', name: 'branch', trim: true), 
        choice(choices: ['staging', 'sandbox', 'prod'], name: 'env')
        ])])
    stage('checkout'){
        git branch: params.branch,url: 'https://github.com/ddu608/allure-junit-example.git'
    }
    
    def parallelSample = [:]
    
    parallelSample["compile"] ={
        compile()
    }
    
    parallelSample["refreshDB"]={
        refreshDB()
    }
    parallelSample.failFast = true
    parallel parallelSample
    
    stage('deploy it to test env'){
        echo "deploy it to ${params.env}"
    }
    stage('testing'){
        sh '''
            ./mvnw test -Dtest=!SearchTest
        '''
        junit '**/target/surefire-reports/*.xml'
    }
}
