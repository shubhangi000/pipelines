pipeline
{
agent any      // if agent is declared before stages, means it is a global agent,
              // here "any" means run follwing stages on any available executor

stages         // it contains all the stages
{
   stage('stage-1')
   { steps                                  //how to perform stage-1
     {  sh 'echo hi, this is jenkins'       // jenkins executes steps in sequence
        sh 'echo hi, this is prakash'  }    // sh represents to linux shell where you can the job
   }

   stage('stage-2-code build')              //jenkins executes stages in sequence
   { steps
      { sh 'echo code_is_building' }
   }

  
}
}

