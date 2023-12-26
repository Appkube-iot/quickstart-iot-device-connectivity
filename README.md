# quickstart-iot-device-connectivity
Automated Cloud Environment Setup for IOT backbone

## How to deploy the cloud environment
This project gets deployed to the Aws through the AWS code pipeline.
Please go to the following directory
iot-onboarding-code-pipelines 
run deploy.sh specifying the environment to deploy. That will call other code pipelines that will depploy the 
infra / data processing / service / sitewise / quicksights configuration.

ONce the stack is deployed , you can see the cloud formation stack output in the AWS Console and find out the deplyed environment details , like what bucket got created , api endpoints etc. A config file details for that environment is stored in the S3 bucket.

## How to test the device registration and connectivity

 export bucket=iotonboardingcodepipelin-iotonboardingartifacts02-1x3qxi4duzifq
 export env=dev
 run the test file
 papu@papu:/opt/mycode/appkube/quickstart-iot-device-connectivity/e2e$ ./test.sh $env $bucket

The test script register a device and tests mqtt communications.


