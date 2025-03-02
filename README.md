# Claude 3.7 Sonnet - AWS Bedrock Interaction Notebook

## Overview
This Jupyter Notebook tells you how to work with **thinking mode** and **images** when interacting with **Claude 3.7 Sonnet** via **AWS Bedrock**. It explains how to send text prompts, attach images, and use structured reasoning before generating responses.

## Features
- **AWS Bedrock Integration**: Uses AWS SDK (`boto3`) to send requests to Claude 3.7 Sonnet.
- **Thinking Mode**: Enables step-by-step reasoning before generating answers.
- **Dynamic Prompt Handling**: Accepts both text-only and text-with-image prompts.

## Requirements
Before running the notebook, ensure you have the following installed:
- Python 3.12+
- `boto3`
- `python-dotenv`

## Setup
1. **Install Dependencies:**
   ```bash
   pip install boto3 python-dotenv
   ```
2. **Configure AWS Credentials:**
   - Create a `.env` file and add your AWS credentials:
     ```ini
     AWS_ACCESS_KEY_ID=your_access_key
     AWS_SECRET_ACCESS_KEY=your_secret_key
     ARN=your_model_arn
     ```

## Usage
1. Load AWS credentials from `.env`.
2. Initialize the AWS Bedrock client.
3. Call `invoke_claude_with_image(prompt, image_path, enable_thinking)`:
   - `prompt`: Input text prompt.
   - `image_path`: (Optional) Path to an image file.
   - `enable_thinking`: (Optional) Enables structured reasoning.

## Example
```python
response = invoke_claude_with_image("Describe this image.", "sample.jpg", enable_thinking=True)
print(response)
```

## Notes
- Ensure AWS Bedrock is enabled in your AWS account.
- Use images in `JPEG` format when attaching to prompts.
- Thinking mode helps generate structured reasoning before answers.

## License
This project is for educational purposes. Modify and use it as needed!

