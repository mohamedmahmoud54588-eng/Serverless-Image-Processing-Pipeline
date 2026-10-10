# Project 2: Serverless Image Processing Pipeline

## Architecture
Serverless / Event-Driven Architecture on AWS[span_0](start_span)[span_0](end_span).

## Description
This project builds a fully automated, serverless image processing pipeline[span_1](start_span)[span_1](end_span)[span_2](start_span)[span_2](end_span). When a user uploads an image to an Amazon S3 source bucket, it triggers an event to an SQS queue[span_3](start_span)[span_3](end_span)[span_4](start_span)[span_4](end_span). An AWS Lambda function polls the queue, processes the image (resizes or adds a watermark), and saves the final result into a destination S3 bucket[span_5](start_span)[span_5](end_span)[span_6](start_span)[span_6](end_span). Amazon CloudFront is used to deliver the processed images globally with low latency[span_7](start_span)[span_7](end_span).

## Key AWS Services Used
* **Amazon S3:** Used for source and destination storage, managing bucket policies, and lifecycle rules[span_8](start_span)[span_8](end_span).
* **Amazon SQS:** Decouples events from processing and acts as a buffer for reliability[span_9](start_span)[span_9](end_span).
* **AWS Lambda:** Executes the image resizing and watermarking logic without managing servers[span_10](start_span)[span_10](end_span).
* **Amazon Step Functions:** Orchestrates multi-step workflows (validation, resizing, metadata extraction)[span_11](start_span)[span_11](end_span).
* **Amazon DynamoDB:** Stores image metadata like upload time, dimensions, and status[span_12](start_span)[span_12](end_span).
* **Amazon CloudFront:** Delivers processed images globally to users with low latency[span_13](start_span)[span_13](end_span).

## Learning Outcomes
* Designing event-driven architectures using S3 event notifications and SQS[span_14](start_span)[span_14](end_span).
* Understanding how message decoupling improves application resilience[span_15](start_span)[span_15](end_span).
* Orchestrating multi-step serverless workflows using Step Functions[span_16](start_span)[span_16](end_span).
* Applying S3 lifecycle policies to manage storage efficiently[span_17](start_span)[span_17](end_span).
