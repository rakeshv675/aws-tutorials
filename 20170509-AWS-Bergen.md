# AWS meetup Bergen 2017-05-09

## Tutorial #1
Intention is to protect your account
* Assigning MFA to user
  * Take a look in IAM
  * Set MFA on the root account

## Tutorial #2
Intention is to protect your account with an audit log

* Turn on and check out cloud-trail

## Tutorial #3
Intention is to use S3 to host webpages. 

* Make a simple webserver
  * Make a bucket in S3
  * Configure it to act as a webserver
  * Upload some content (html, img…)

Hints:
* Bucket policy
* Static Website Hosting

Cleanup: Remove bucket

## Tutorial #4
This tutorial set up a load balanced redundant web-envronment in PHP. Use this to explorer how loadbalancing and autoscaling works. After the system is up and running, check out the setup of Loadbalancers and Autoscaling in the EC2-console. Also try to adjust number og hosts, shutdown a host etc. Whan you have more than one server running, deloy a new versjon of the application.

* Start a Beanstalk-stack via “Get Started”
  * webserver environment
  * PHP and Load balancing
  * application 
    * https://s3-eu-west-1.amazonaws.com/anders-aws-bucket/awsdemo/HelloAWS.zip
    * https://s3-eu-west-1.amazonaws.com/anders-aws-bucket/awsdemo/HelloAWS2.zip
  * Configure more
    * high availability
    * environment settings
     * sett URL
    * Instances
     * type t2.micro
    * network
      * create environment inside VPC
      * select all subnets for ELB og EC2
      * make load balancer public available
  * Create app  (takes aprox 5 mins)
  
Things to try and see:
  * Check settings for loadbalancer and autoscaling on EC2-console
  * Open the application in a browser-windows (or more). The page will reload ever 5 sec. 
  * Adjust number of servers
  * Deploy a new version of the app 
  * Shutdown a server (EC2-console)

## Tutorial #5
Set up a serverless event-driven system for processing files:
https://github.com/abjoerne/lambda-refarch-fileprocessing

## Tutorial #6
Set up a photo-album with automatic resize of photos and tagging of content
https://github.com/awslabs/lambda-refarch-imagerecognition

