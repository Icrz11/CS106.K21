# Chúng em Demo 2 chương trình:
### Chương trình 1 bao gồm 2 file
1. DoAnAI - file này chứa source code toàn bộ chương trình bao gồm Tiền xử lí dữ liệu, Rút trích đặc trưng, Chọn thuật toán, Tuning model
2. DemoAI - file này dùng để Demo cho chương trình 1 này
Bên trong file Demo AI chứa biến Link - đây là biến đầu vào của chương trình chứa đường dẫn tới 1 ảnh (là file raw).
Thay đổi giá trị biến Link này để dẫn tới các ảnh khác.

### Chương trình 2:
- Chứa cách tải,sử dụng model có sẵn VGG-16 - quá trình Transfer learning - để rút trích đặc trưng. Sau đó được học bằng MLP ở 3 lớp Dense cuối.
- Phần load lại model và dùng model để dự đoán hình ảnh sẽ ở phần cuối "Load Model". 

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
