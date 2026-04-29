# aws-s3-static-website-versioning-replication

🚀 S3 Static Website Hosting with Versioning & Cross-Region Replication

📌 Project Overview

This project demonstrates how to build a highly available static website using Amazon S3 with advanced features like versioning and cross-region replication.

The goal is to simulate a real-world cloud architecture where data is durable, recoverable, and globally available.

🏗️ Architecture
<img width="279" height="339" alt="Untitled Diagram" src="https://github.com/user-attachments/assets/8e9e5187-053e-4dda-a848-9a9351c4a642" />

⚙️ Services Used

* Amazon S3 (Static Website Hosting)
  
* S3 Versioning
  
* S3 Cross-Region Replication (CRR)
  
* IAM Role (for replication permissions)

  🛠️ Implementation Steps

1. Primary S3 Bucket Creation

* Created bucket: fao-demo-s3-v1
  
* Region: us-east-1 (N. Virginia)
  
* Disabled block public access
  
* Enabled Versioning
  
* Configured Bucket Policy for public access
  
 <img width="1512" height="982" alt="1" src="https://github.com/user-attachments/assets/df1f8452-2583-4978-b48a-dc1c1ec126ab" />
 <img width="1512" height="982" alt="2" src="https://github.com/user-attachments/assets/51322fcb-7eef-43ff-99ea-0d5a4165f69a" />
 <img width="1512" height="982" alt="4" src="https://github.com/user-attachments/assets/a241201d-d7aa-4f7e-8934-167d99d2f94e" />
 <img width="1512" height="982" alt="6" src="https://github.com/user-attachments/assets/cfd940a1-6009-44e3-b028-9c7d0e081a19" />



 2. Static Website Hosting

* Enabled static website hosting
  
* Uploaded:
  
    * index.html
      
    * image assets
      
* Verified website using S3 endpoint URL
<img width="1512" height="982" alt="5" src="https://github.com/user-attachments/assets/9a7caecc-b42b-4c62-8641-c8b3b3861f13" />
<img width="1512" height="982" alt="7" src="https://github.com/user-attachments/assets/7f1b7a75-5b24-4ca5-9a81-281fb7ba84bf" />
<img width="1512" height="982" alt="9" src="https://github.com/user-attachments/assets/0de6e36c-19c8-4a1e-8d11-67261ca6ed8e" />
<img width="1512" height="982" alt="10" src="https://github.com/user-attachments/assets/1d93bea9-bfb0-4857-a1d1-afad16a1d5e6" />

3. Versioning Implementation

* Uploaded multiple versions of index.html
  
* Observed:
  
    * Old version retained
      
    * New version active
      
* Verified version control and rollback capability

  
<img width="1512" height="982" alt="11" src="https://github.com/user-attachments/assets/1f85d0f1-fc29-414b-bd08-9381568df34e" />
<img width="1512" height="982" alt="12" src="https://github.com/user-attachments/assets/233ec51c-4ef3-4758-8a17-dd45b11b13fd" />
<img width="1512" height="982" alt="13" src="https://github.com/user-attachments/assets/6c9a35cf-0c13-4e77-a50c-7484bf78c85f" />
<img width="1512" height="982" alt="14" src="https://github.com/user-attachments/assets/e4ddbcdf-f463-49de-b119-2246cd1c2d2b" />
<img width="1512" height="982" alt="15" src="https://github.com/user-attachments/assets/20597a8d-9ab6-4f38-9a28-caf5dc2df4b6" />

4. Cross-Region Replication

* Created replica bucket: fao-demo-s3-replica-v2
  
* Region: ap-southeast-1 (Singapore)
  
* Enabled versioning on replica bucket
  
* Configured replication rule:
  
    * Source: Primary bucket
      
    * Destination: Replica bucket
      
* Created and attached IAM role for replication

  <img width="1512" height="982" alt="16" src="https://github.com/user-attachments/assets/c079d3f8-f91f-4d18-b2d0-26a0d223d77a" />
  <img width="1512" height="982" alt="17" src="https://github.com/user-attachments/assets/b2845fa5-9e85-485e-a0e8-242ee0675494" />
  <img width="1512" height="982" alt="18" src="https://github.com/user-attachments/assets/c6d9c20d-32ff-454b-bf89-4eac6d86ab08" />

  5. Replication Testing

* Uploaded new objects to primary bucket
  
* Verified automatic replication to replica bucket
  
* Checked public object access via URL
  <img width="1512" height="982" alt="19" src="https://github.com/user-attachments/assets/f329183b-91be-4fbd-8947-398d2f0cc7e5" />

🎯 Key Features

* ✅ Static website hosting using S3
  
* ✅ Object versioning (data protection)
  
* ✅ Cross-region replication (high availability)
  
* ✅ Public access configuration
  
* ✅ Real-time replication testing

⸻

💡 Why This Project Matters

🔹 Scalability

S3 allows hosting static websites that can scale automatically without managing servers.

🔹 Data Protection

Versioning ensures that older versions of files are preserved, preventing accidental data loss.

🔹 High Availability

Cross-region replication ensures your data is available even if one AWS region fails.

🔹 Cost Efficiency

S3 provides a low-cost solution compared to traditional server-based hosting.

⸻

🧠 What I Learned

* How to host a static website using S3
  
* How S3 versioning works in real scenarios
  
* How to configure cross-region replication
  
* IAM role usage for secure service communication
  
* Real-world cloud architecture for availability and durability

  🚀 Future Improvements

* Add CloudFront (CDN) for faster global delivery
  
* Implement HTTPS using custom domain
  
* Add logging & monitoring (CloudWatch)

⸻

👨‍💻 Author

Faisal Ahmed Ome

⸻

🔥 Conclusion

This project demonstrates a real-world cloud storage architecture using AWS S3 with features like versioning and replication, ensuring **data durability, availability, and scalabilit
  




