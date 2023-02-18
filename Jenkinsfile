/*
 See the documentation for more options:
 https://github.com/jenkins-infra/pipeline-library/
*/
pipeline {
  agent any
  
  stages {
    stage('Detect Language') {
      steps {
        languageDetector(
          filePattern: '**/*.java', // Path to the files you want to detect language for
          outputFile: 'languages.json' // Output file to store the detected languages
        )
      }
    }
    
    stage('Print Language') {
            steps {
                sh "echo Detected language: ${env.LANGUAGE}"
           
            }
        }
  }
}

