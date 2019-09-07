# Face_Recognize
- Cấu trúc:
- align: thư mục dùng để chuẩn bị dữ liệu\\
	- |--- train_img:	thư mục dùng để chứa ảnh người mình muốn nhận dạng\\
	- |--- pre_img:		thư mục sau khi dùng mtcnn để để căn chỉnh và cắt mặt\\
	- |--- det1.npy, det2.npy, det3.npy: các file chứa trọng số của mtcnn\\
	- |--- detect_face:	file chính của mtcnn (cấu trúc mạng, xử lý)\\
	- |--- initializer.py:	file dùng cắt mặt sau đó mặt được cắt sẽ cho vào file 'pre_img'\\
- model_pretrained: 
	- |--- tải file model pretrained trong file txt, sau đó để giải nén để file 201804002-1147759.pb vào trong này\\
	- |--- 201804002-1147759.pb: file pre-trained model của mạng inception-resnet v1\\

- classifier.py: file dùng để phân loại các mặt của cùng 1 người sử dụng SVM

- facenet.py: mục đích load model inception_resnet v1, load dữ liệu

- predict.py: file dùng để dự nhận diện mặt người - "python predict.py ten_anh_muon_nhan_dien 201804002-1147759.pb classifier.pkl"

- classifier.pkl: file chứa trọng số huấn luyện SVM
