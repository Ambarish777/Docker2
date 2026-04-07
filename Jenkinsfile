pipline{
  agent any
  stages{
    stage('#1.Chekout'){
      steps{
        git url:"https://github.com/Ambarish777/Docker2",branch:"main"
      }
    }

    stage('#2. Build the image'){
      steps{
        bat 'docker build -t mywebsite .'  
      }
    }

    stage('#3. Stop all old containers'){
      steps{
        bat 'docker stop mycont || exit 0'  
        bat 'docker rm mycont || exit 0'
      }
    }

    stage('#4. Run the Image - Containerise'){
      steps{
        bat 'docker run -d -p 9999:80 --name mycont mywebsite'
      }
    }
  }
}
