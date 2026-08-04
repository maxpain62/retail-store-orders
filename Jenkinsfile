podTemplate(yaml: readTrusted('pod.yaml')) {
    node(POD_LABEL) {
        stage('checkout') {
            git branch: 'main', url: 'https://github.com/maxpain62/retail-store-orders.git'
        }
        stage('build') {
            container('java-build') {
                sh'''
                ./mvnw -DskipTests clean package
                '''
            }
        }
    }
}