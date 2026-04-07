pipline{
  agent any
  stages{
    stage('#1.Chekout'){
      steps{
        git url:'https://github.com/Ambarish777/Docker2',branch:"main"
      }
    }

    stage('#2. Build the image'){
      steps{
        bat 'docker build -t mywebsite .'  //mywebsite-imagename
      }
    }

    stage('#3. Stop all old containers'){
      steps{
        bat 'docker stop mycont || exit 0'   //mycont-containername
        bat 'docker rm mycont || exit 0'
      }
    }

    stage('#4. Run the Image - Containerise'){
      steps{
        bat 'docker run -d -p 6001:80 --name my cont mywebsite'
      }
    }
  }
}
