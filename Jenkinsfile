pipeline {
agent any
tools { nodejs 'node22' }
triggers { pollSCM('H/2 * * * *') }
stages {
stage('Installer') { steps { sh 'npm ci --include=optional' } }
stage('Tester') { steps { sh 'npm test' } }
}
}