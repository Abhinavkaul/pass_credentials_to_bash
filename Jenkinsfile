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
          //withCredentials([usernamePassword(credentialsId: 'git_credentials', passwordVariable: 'pass', usernameVariable: 'user')]) 
          //{
            bat "git tag -d 0.0.13"
           bat "git tag 0.0.13"
            echo "hello avi"
          sshagent(['personal_git_ssh']) 
          {
            bat "git push --tags"
           }
            //bat "git push origin 0.0.13"
          //}
        }
      }
    }
  }
}
