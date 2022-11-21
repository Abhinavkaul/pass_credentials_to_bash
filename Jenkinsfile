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
            echo "this is password '$Pass'"
          }
        }
      }
    }
  }
}
