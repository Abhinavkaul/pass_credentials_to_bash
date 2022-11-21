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
          echo "abc"
          echo "Stage: Build number: $BUILD_NUMBER"

          bat ("echo Shell: Build number: $BUILD_NUMBER")

          bat ("demo.sh")
        }
      }
    }
  }
}
