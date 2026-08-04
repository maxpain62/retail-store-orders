podTemplate(yaml: readTrusted(pod.yaml)) {
    node(POD_LABEL) {
        stage('checkout') {
            git branch: 'main', url: 'https://github.com/maxpain62/retail-store-order.git'
        }
    }
}