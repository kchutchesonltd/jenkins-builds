pipeline {
  agent any
  stages {
    stage('BuildStep1') {
      parallel {
        stage('BuildStep1') {
          steps {
            sh '''echo "Build Step 1"
echo $BUILD_ID
echo $WORKSPACE
ls -la $WORKSPACE




cat > $WORKSPACE/file1 <<EOF
something
EOF
cat > $WORKSPACE/file2 <<EOF
something
EOF'''
          }
        }

        stage('BuildStep2') {
          steps {
            sh '''echo "Build Step 2"
echo $BUILD_NUMBER
echo $BUILD_URL'''
          }
        }

      }
    }

    stage('Complete') {
      steps {
        echo 'Build Complete'
      }
    }

  }
}