# Demo AWS lambda

Demonstration of Amazon Web Services (AWS) Lambda function setup.

## Sign up

* Sign up for AWS at https://aws.amazon.com

* Sign up for AWS Lamba at https://aws.amazon.com/lambda/


## Create a function

Go to the Lamba dashboard at https://console.aws.amazon.com/lambda/home

  * Click "Create a Lambda function"

Select blueprint:

  * Blueprints are sample configurations of event sources and Lambda functions. There are blueprints for APIs, microservices, data sources, third-party integrations, and more.

  * Click "Blank Function" because we will create our own function.

Configure triggers:

  * Triggers invoke our function, and can come from many AWS areas, such as API Gateway, Alexa, CloudWatch, S3, SNS, etc.

  * Click "Next" to skip this step.

Configure function:

  * Name: myDemoFunction

  * Description: My demo function is great!

  * Runtime: Node.js 4.3

Lambda function code:

  * Code entry type: Edit code inline

  * The edit box shows:

      exports.handler = (event, context, callback) => {
        // TODO implement
        callback(null, 'Hello from Lambda');
      };

Lambda function handler and role:

  * Handler: index.handler

  * Role: Create a new role from template(s)

  * Role name: myDemoRole

  * Policy templates: Simple microservices permissions

Advanced settings:

  * Use the defaults

Review:
 
  * Click "Create function"

  * You see: Congratulations! Your Lambda function "myDemoFunction" has been successfully created.

  * Your browser now shows the function page. 

  * Notice the URL goes to the function page: https://console.aws.amazon.com/lambda/home?region=us-east-1#/functions/myDemoFunction?tab=code


## Test

If you're following this demo, then you're already on the function page, and you see a big blue "Test" button.

  * Click "Test"

Input test event:

  * Sample event template: Hello World (default)

  * Use the default input source code, which has some keys and values.

  * Click "Save and test"

Results:

  * The results area shows:
    * Execution result: succeeded (logs)
    * `"Hello from Lambda"`

  * The summary area shows:
    * Code SHA-256
    * Request ID
    * Duration
    * Billed duration
    * Resources configured
    * Max memory used

  * The log output shows:
    * START RequestId
    * END RequestId
    * REPORT RequestId
