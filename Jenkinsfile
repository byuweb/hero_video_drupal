pipeline {
  agent any
  stages {
    stage('Pull') {
      steps {
        sh 'git pull origin 8.x-1.x --tags'
        sh 'git pull origin 8.x-1.x'
      }
    }
    stage('Push') {
      steps {
        sh 'git pull git@git.drupal.org:project/hero_video.git refs/heads/8.x-1.x'
        sh 'git push git@git.drupal.org:project/hero_video.git refs/heads/8.x-1.x'
        sh 'git push git@git.drupal.org:project/hero_video.git --tags'
      }
    }
  }
}
