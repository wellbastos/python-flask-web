pipeline {
  agent {
    dockerfile {
      filename 'Dockerfile'
    }

  }
  stages {
    stage('clone git') {
      steps {
        git(url: 'https://github.com/wellbastos/python-flask-web.git', branch: 'master')
      }
    }

    stage('build docker') {
      steps {
        build(quietPeriod: 10, job: 'build docker', propagate: true, wait: true)
      }
    }

  }
}