pipeline {
agent any
stages {
stage('Checkout') {
steps {
git 'https://github.com/v4dis/fooproject/'
}
}
stage('Build') {
steps {
sh "mvn compile"
}
}
stage('Test') {
steps {
sh "mvn test"
}
post {
always {
junit '**/TEST*.xml'
}
}
}
}
}