# aws_projects
Project Overview:
I developed a text-to-speech service using AWS Lambda, Amazon Polly, and S3. The project enables users to input text, which is then converted into an audio file stored in an S3 bucket, providing a link for easy access.

Setting Up AWS Lambda:
• Created a Lambda function in the AWS Management Console using Python.
• Configured the function to call Amazon Polly’s synthesizeSpeech API to convert text into speech.
• Utilized the audio stream returned by Polly and saved it as an MP3 file in an S3 bucket.

S3 Integration:
• Uploaded the audio file to an S3 bucket and configured permissions for public access.
• Generated a public URL for the stored audio file, which can be shared with users for download.

API Gateway Setup:
• Set up an API Gateway to trigger the Lambda function via a POST request.
• Configured the endpoint to accept dynamic text in the request body and return the generated audio file's S3 URL in the response.
• Ensured that CORS and authorization were correctly configured to allow API access.

Testing & Debugging:
• Initially tested the Lambda function using the built-in test feature in the AWS Lambda console.
• Performed end-to-end testing using Postman to ensure the API worked as expected, with accurate audio file generation.

Deployment:
• Deployed the API on a stage in API Gateway and ensured the Lambda function was linked correctly.
• Published the API and tested it with real input to verify that the text-to-speech functionality was working as expected.
