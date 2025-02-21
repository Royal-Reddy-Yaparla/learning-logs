# learning-logs
📅 Date:  (YYYY-MM-DD)

🔹 Topic: (e.g., Terraform Modules)

🛠️ Problem Faced: (e.g., Error in backend S3 configuration)

🧐 Debugging Steps: (What did you try? What worked?)

💡 Solution: (Final fix and explanation)

🚀 Key Takeaways: (What did you learn? Any best practices?)

📌 Reference Links: (Docs, videos, GitHub issues, etc.)

## Example

📅 Date: 2025-02-11  
🔹 Topic: Terraform S3 Backend Issue  
🛠️ Problem Faced: Error "S3 bucket does not exist" during `terraform init`  
🧐 Debugging Steps:  
  1. Verified bucket name in AWS S3 Console ✅  
  2. Checked IAM permissions ✅  
  3. Ran `aws s3 ls` to confirm bucket access ✅  
💡 Solution:  
  - The bucket name was incorrect in `backend "s3" {}`  
  - Fixed it and re-ran `terraform init -reconfigure`  
🚀 Key Takeaways:  
  - Ensure S3 bucket exists **before initializing** Terraform backend.  
  - Use `aws s3 ls` to check bucket access.  
📌 Reference Links:  
  - https://developer.hashicorp.com/terraform/docs/backends/types/s3  
