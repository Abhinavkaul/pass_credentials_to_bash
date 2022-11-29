pipeline
{
  agent any
  stages
  {
    stage("requirements")
    {
      steps
      {
        script
        {
          withCredentials([usernamePassword(credentialsId: 'rought_delete_it', passwordVariable: 'Pass', usernameVariable: 'Abhi')]) 
          {
          echo "abc"
          echo "this is variable '$Abhi'"
          }
        }
      }
    }
    stage("push tags")
    {
      steps
      {
        script
        {
          withCredentials([usernamePassword(credentialsId: 'git_credentials', passwordVariable: 'pass', usernameVariable: 'user')]) 
          {
           bat "git tag 0.0.13"
            echo "hello avi"
            bat "git push https://${user}:${pass}@github.com/Abhinavkaul/pass_credentials_to_bash.git --tags"
          }
        }
      }
    }
  }
}
