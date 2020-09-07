pipeline {
     agent any
     stages {
         stage('Upload to AWS) {
             targetBuckets.each {
                 withAWS(region: 'us-west-2') {
                     s3Upload(file: 'index.html', bucket: 'jenkins-pipeline-aws', acl:'BucketOwnerFullControl')
                 }
             }
         }
     }
}
