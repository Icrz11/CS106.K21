
Model configs:
https://drive.google.com/file/d/1-2A6Ur_aMdopQn1jR6S2mvNualeyE-lw/view?usp=sharing

Model weights:
https://drive.google.com/file/d/1--MDCFnK20QN-lGezqp9uO-zk6dU80_k/view?usp=sharing


Script for download model Weight:

For instance id for download weights would be:
	1--MDCFnK20QN-lGezqp9uO-zk6dU80_k

### Using drive-link:
	from pydrive.auth import GoogleAuth
	from pydrive.drive import GoogleDrive
	auth.authenticate_user()
	gauth = GoogleAuth()
	gauth.credentials = GoogleCredentials.get_application_default()
	drive = GoogleDrive(gauth)
	file_id = "YOUR_FILE_ID"
	downloaded = drive.CreateFile({'id': file_id})
	downloaded.GetContentFile(os.path.join(data_dir, 'file_name.zip'))