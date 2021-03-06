# Serverless.yml Reference
Here is a list of all available properties in serverless.yml when the provider is set to tencent.
```yaml
# Welcome to Serverless!
#
# This file is the main config file for your service.
# It's very minimal at this point and uses default values.
# You can always add more config options for more control.
# We've included some commented out config examples here.
# Just uncomment any of them to get that config option.
#
# For full config options, check the docs:
#    docs.serverless.com
#
# Happy Coding!

service: my-service # service name

provider: # provider information
  name: tencent
  runtime: Nodejs8.9 # Nodejs8.9 or Nodejs6.10
  credentials: ~/credentials

# you can overwrite defaults here
#  enableRoleAuth: true
#  stage: dev
#  cosBucket: DEFAULT
#  role: QCS_SCFExcuteRole
#  memorySize: 256
#  timeout: 10
#  region: ap-shanghai
#  environment:
#    variables:
#      ENV_FIRST: env1
#      ENV_SECOND: env2
#  vpcConfig:
#    vpcId: test
#    subnetId: test

plugins:
  - serverless-tencent-scf

# you can add packaging information here
#package:
#  include:
#    - include-me.js
#    - include-me-dir/**
#  exclude:
#    - exclude-me.js
#    - exclude-me-dir/**

functions:
  function_one:
    handler: index.main_handler
#    description: Tencent Serverless Cloud Function
#    runtime: Nodejs8.9 # Nodejs8.9 or Nodejs6.10
#    memorySize: 256
#    timeout: 10
#    environment:
#      variables:
#        ENV_FIRST: env1
#        ENV_Third: env2
#    vpcConfig:
#        vpcId: test
#        subnetId: test
#    events:
#      - timer:
#          name: timer
#          parameters:
#            cronExpression: '*/5 * * * *'
#            enable: true
#      - cos:
#          name: cli-appid.cos.ap-beijing.myqcloud.com
#          parameters:
#            bucket: cli-appid.cos.ap-beijing.myqcloud.com
#            filter:
#              prefix: filterdir/
#              suffix: .jpg
#            events: cos:ObjectCreated:*
#            enable: true
#      - apigw:
#          name: hello_world_apigw
#          parameters:
#            stageName: release
#            serviceId:
#            httpMethod: ANY
#            integratedResponse: true
#            path: /abc/cde
#            enableCORS: true
#            serviceTimeout: 10
#      - cmq:
#          name: cmq_trigger
#          parameters:
#            name: test-topic-queue
#            enable: true
#      - ckafka:
#          name: ckafka_trigger
#          parameters:
#            name: ckafka-2o10hua5
#            topic: test
#            maxMsgNum: 999
#            offset: latest
#            enable: true

```
