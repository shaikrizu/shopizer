node {
     stage('packege') {
   sh'cd shopizer'
  }
   stage('packege') {
   sh'mvn clean install'
  }
  stage ('copy war file s3') {
  s3Upload consoleLogLevel: 'INFO', dontWaitForConcurrentBuildCompletion: false, entries: [[bucket: 'shopizer-s3', excludedFile: 'target/shopizer.war', flatten: false, gzipFiles: false, keepForever: false, managedArtifacts: false, noUploadOnFailure: false, selectedRegion: 'us-east-1', showDirectlyInBrowser: false, sourceFile: '**/target/*.war', storageClass: 'STANDARD', uploadFromSlave: false, useServerSideEncryption: false]], pluginFailureResultConstraint: 'FAILURE', profileName: 's3', userMetadata: []
  }
  }
