def branch = 'main'
def repoUrl = 'https://bitbucket.example-group.com/scm/xxx/example-app.git'
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
            sh '''
          git config --global credential.username $user
          git config --global credential.helper '!f() { echo password=$pass; }; f'
          '''
           sh "git tag 0.0.6"
            sh "git push ${repoUrl} --tags"
          }
        }
      }
    }
  }
}
