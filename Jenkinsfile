pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'npm i -g yarn'
        sh 'yarn format'
        sh 'yarn build'
      }
    }

    stage('Test') {
      steps {
        sh 'yarn start'
      }
    }

  }
  environment {
    DISCORD_TOKEN = 'ODkxOTE4OTYwOTUyNDkyMDcy.GDvgfB.4T2zR1PqimwYk4gJ9wbkEYXISy7HG4bgNheZBw'
    GUILD_ID = '891914113599549480'
    STARBOARD_CHANNEL_ID = '1018615137395024012'
    DB_CONN_STRING = 'postgres://user:admin@localhost:5555/adnauseam'
    PISTON_URL = 'localhost'
  }
}