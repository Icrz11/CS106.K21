
Model configs:
https://drive.google.com/file/d/1-2A6Ur_aMdopQn1jR6S2mvNualeyE-lw/view?usp=sharing

Model weights:
https://drive.google.com/file/d/1--MDCFnK20QN-lGezqp9uO-zk6dU80_k/view?usp=sharing


Script for download model Weight:

### Using drive-link:
	from pydrive.auth import GoogleAuth
	from pydrive.drive import GoogleDrive
	auth.authenticate_user()
	gauth = GoogleAuth()
	gauth.credentials = GoogleCredentials.get_application_default()
	drive = GoogleDrive(gauth)
	file_id = "YOUR_FILE_ID"
	# For example: "1-sltCi9nCSQmA-xaBPutq6Yfl6YONC_H" id of Tokenizer file
	downloaded = drive.CreateFile({'id': file_id})
	downloaded.GetContentFile(os.path.join(data_dir, 'file_name.zip'))