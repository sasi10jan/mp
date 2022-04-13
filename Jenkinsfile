pipeline {
agent any
stages {
stage('Build') {
steps {
  bat 'mvn -B -U -e -V clean -DskipTests package'
}
}

 stage('Test') {
      steps {
          bat "mvn test"
      }
    }
    
stage('Deploy') {
steps {
echo 'Deploying mule project due to the latest code commit…'
echo 'Deploying to the configured environment….'
  
  bat 'mvn clean deploy -DmuleDeploy -DskipTests'

}
}
}
}
