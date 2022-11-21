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
          echo "def"
          bat ("echo Shell: Build number: $BUILD_NUMBER")
          echo "ghi"
          bat ("demo.sh")
        }
      }
    }
  }
}
