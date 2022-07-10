# Pipeline Process

The pipeline process involves the automated Continuous Integration and Continuous Development of the software life-cycle.

## Software Development

This step starts with code development. 
Once a developer has committed their code and pushed it to the linked github account we move to the next step.

## Circle CI

Circle CI detects changes on the github account, to which it is linked, and triggers a predefined Pipeline execution.

## Pipeline

In advance we define a set of operations to complete when software changes, eg. new features, bug squashing, etc.
The automated pipeline executes the relevant workflows and specific jobs, these are detailed below together with a short description. 

### Build

During the `Build` phase the software changes are checked to make sure that they integrate with the existing code. 

The following jobs are completed: 

* Spin up environment ( create the working environment )
* Prepare environment variables ( utilises the predefined env-vars )
* Install Node 
* Code Checkout ( copies the code from the github repository )
* Install dependencies FE & BE ( ensures no breaking dependencies )
* Front-End Lint ( Lints the Angular App )
* Front-End Build  ( makes sure the FE can be built with the software changes )
* API Build ( checks changes allow the API, BE, to be built )



### Hold

After the `Build` jobs completes and is successful, there is a `Hold` on any further pipeline execution. 

Before the pipeline can continue we must manually `Approve` the build from the circleci dashboard. 

Once the `Build` is `Approved` we proceed to the deployment phase.

### Deploy

During the `Deploy` the following jobs will be completed: 

* Spin up environment ( create the working environment )
* Prepare environment variables ( utilises the predefined env-vars )
* Install Node 
* Code Checkout ( copies the code from the github repository )
* Install AWS CLI ( this allows aws command scripts to be executed )
* Configure AWS Access Key ID ( provides authentication and authorisation )
* Setting Up Elastic Beanstalk CLI ( provides the EB CLI environment to execute `eb deploy`)
* Deploy ( executes dependency installs, builds and deployments in a single job )

The last step in deployment is the most interesting of all the jobs during the `Deploy` phase.
Explicitly, once the `Build` phase has completed, the `Deploy` phase takes it one step further having already confirmed that the software changes are viable and will be functional.

The deployment is then processed to our infrastructure, namely, our S3 Buckets and our Elastic Beanstalk environment. 

## Pipeline Diagram




<img src="pipeline_diagram.png" >





