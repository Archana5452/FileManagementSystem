------------------------------------------------------------------
--- File Management System (FMS) with Cloud-Powered Backend and Django Framework. ---
------------------------------------------------------------------
![image](https://github.com/Archana5452/FileManagementSystem/assets/135411348/3ccc2d28-dea5-48a5-ad2f-8b635f5e5c3a)


Welcome to the File Management System (FMS), a web-based application designed to simplify the storage, upload, management, and sharing of files. FMS is a versatile solution crafted for various users to efficiently handle documents, ensuring accessibility and organization. The cloud-powered backend, built on the Django framework, enhances the system's capabilities, providing scalable hosting, managed database services, and reliable file storage through AWS cloud services. FMS is an ideal tool for users seeking an intuitive and secure platform for seamless file management, with the added benefits of cloud integration for enhanced performance and accessibility.

### Key Features and Functionalities:

1. **Authentication System:**
   - Users must log in to upload files, ensuring secure access.

2. **File Information:**
   - Each uploaded file includes title and description fields for quick identification and retrieval.

3. **Shareable Links:**
   - The system generates shareable links, facilitating easy sharing of specific files among authenticated users.

4. **Download Files:**
   - Users can download files directly from the system for offline access.

5. **AWS Cloud Integration:**
   - **Amazon EC2 for Hosting:**
     - Utilizes Amazon EC2 to host the application, providing scalable and reliable computing resources.
   - **Elastic IP for Stability:**
     - An Elastic IP is associated with the EC2 instance for a stable external endpoint, ensuring consistent accessibility.
   - **Amazon RDS for Database Management:**
     - Amazon RDS for PostgreSQL manages the database, ensuring scalability, managed data storage, and simplified database administration.
   - **Amazon S3 for File Storage:**
     - Leverages Amazon S3 for scalable and durable file storage, enhancing reliability and accessibility.

6. **Profile Management:**
   - Users can update their profile details, ensuring accurate information.

7. **Password Management:**
   - Users have the ability to update their account password for security purposes.

### Technologies Used:

- Python
- Django
- AWS (EC2,S3,RDS)
- HTML
- CSS
- JavaScript
- Bootstrap v5

### Why Cloud Services?

#### Scalability and Reliability:
   - By hosting on Amazon EC2 and using services like RDS and S3, the application achieves scalability and reliability, ensuring consistent performance even with increased data and user demands.

#### Accessibility and Stability:
   - The association of an Elastic IP with the EC2 instance guarantees a stable external endpoint, providing uninterrupted access to the application.

#### Managed Database:
   - Amazon RDS simplifies database management tasks, allowing developers to focus on application development rather than database administration.

#### Scalable File Storage:
   - Amazon S3, a scalable object storage service, provides durable and scalable file storage, accommodating the growing volume of files efficiently.

### How to Run:

#### Step One: Download/Install the following:
- Python (v3.9.1)
- Django (v4.0.3)
- PIP (for Python module installation)

#### Step Two: AWS Cloud Setup:
   1. Set up an Amazon EC2 instance for hosting the application.
   2. Associate an Elastic IP with the EC2 instance for a stable external endpoint.
   3. Utilize Amazon RDS for PostgreSQL to manage the database.
>>> Settings.py (update the database Name,User,Password,Host)

				DATABASES = {
				    "default": {
					"ENGINE": "django.db.backends.postgresql",
				    	"NAME": "postgres",
					"USER": "XXXXXXXX",
					"PASSWORD": "XXXXXXXXX",
					"HOST": "database-2.cbw5rxvx0i1x.ap-south-1.rds.amazonaws.com",
					"POST": "5432",
					}
				} 				
					   
 4. Leverage Amazon S3 for scalable and durable file storage.
>>> Settings.py (Update the AWS ACCESS_KEY,SECRET_ACCESS_KEY, BUCKET)
						
			AWS_ACCESS_KEY_ID ='XXXXXXXXXXXXXX'
			AWS_SECRET_ACCESS_KEY = 'XXXXXXXXXXXXXXXX'
			AWS_STORAGE_BUCKET_NAME = 'XXXXXXXXXXX'
			

#### Step Three: Setup/Installation:
1. Download and Extract the provided source code zip file in ec2 instance.
2. Open your Terminal/Command Prompt window (ensure "python" and "pip" are in your environment variables).
3. Change the working directory to the extracted source code folder (e.g., `cd C:\Users\Downloads\fms`).
4. Run the following commands:
   - `pip install Django`
   - `pip install -r requirements.txt`
   - `python manage.py migrate`
   - `python manage.py runserver 0.0.0.0:8000`
   
#### Step Four: Access the Application:
   - Open a web browser and browse [http://<Elastic-IP>:8000/](http://<Elastic-IP>:8000/) 

