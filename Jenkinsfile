node {
    checkout scm
    stage('Clean') {
        // Clean files from last build.
        sh 'git clean -dfxq'
    }
    stage('Setup') {
        // Prefer yarn over npm.
        sh 'yarn install || npm install'
        dir('client')
        {
            sh 'yarn install || npm install'
        }
    }
    stage('Test') {
        sh 'npm run startpostgres && sleep 10 && npm run migratedb:dev'
        sh 'npm run test:nowatch'

        dir('client')
        {
            sh 'npm run test:nowatch'
        }
        sh 'yarn add jasmine-reporters'

        sh 'npm run startserver:tests & npm run apitest:nowatch && npm run loadtest:nowatch $$ sleep 10 $$ kill $!'

        junit '**/TestReports/*.xml'
    }
    stage('Deploy') {
        sh './dockerbuild.sh'
        dir('./provisioning')
        {
            sh "./provision-new-environment.sh"
        }
    }
}
