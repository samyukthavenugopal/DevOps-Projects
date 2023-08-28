# AWS S3 Event Triggering
### S3 Event triggering is a very popular shell scripting used by lots of companies including Netflix, Airbnb, Adobe, Expedia, and Others.
- Netflix: Netflix uses S3 event triggering to automatically process video files uploaded to Amazon S3, enabling seamless content ingestion and processing.
- Airbnb: This lodging and homestays aggregator uses S3 event triggering to automatically process and analyze data stored in Amazon S3, such as guest reviews and booking information.
- Expedia: They use S3 event triggering to automatically process and analyze data stored in Amazon S3, such as travel bookings, user profiles, and pricing information, to power their personalized travel recommendations and search features.
  
## How S3 Event Triggering Works
- The Amazon S3 notification feature enables you to receive notifications when a certain event occurs inside your S3 Storage bucket. To get notifications, first, add a notification configuration that reads the event you want Amazon S3 Bucket to publish and the destination where Amazon S3 will send the notifications. This configuration is stored in the notification sub-resource that is associated with a bucket.
  
![AWS S3 Event Triggering](https://github.com/samyukthavenugopal/DevOps-Projects/assets/71750386/6d0a305b-d996-4449-a31a-574fe2d4340f)
- Each time a new video/series/documentary is uploaded in the S3 Storage Bucket, you receive a notification. Most organizations use S3 since it is cost-efficient.
- Under the hood, the S3 bucket triggers Lambda Function. Since Lambda is a serverless compute, it allows you to run code that can be written in any programming language. Also, it follows Pay As You Go pricing where you are charged based on the usage.
- This information is sent to SNS (Simple Notification Service), which is a fully managed messaging service provided by Amazon Web Services (AWS). SNS provides reliable message delivery, scalability, and fault tolerance, making it suitable for building robust and scalable messaging systems in the cloud.
- From SNS, it depends from platform to platform. If it is a simple blog posting website, the content can be stored in a S3 bucket and email notifications can be sent to all the subscribers. Whereas in the case of Netflix, there would be some additional queuing, transcoding the video to different formats, extracting metadata, or performing other media processing tasks.
- IAM (Identity and Access Management) allows you to create and manage roles, which are sets of permissions that can be used to access AWS resources, such as EC2 instances, Lambda functions, or other services. In this specific scenario, the Lambda function needs to have permission to be invoked by S3 Bucket and invoke SNS. Hence we will need to grant IAM permission to Lambda Function.

