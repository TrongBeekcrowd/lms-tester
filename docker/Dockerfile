# Sử dụng hình ảnh cơ bản của Python
FROM python:3.9-slim

# Thiết lập thư mục làm việc
WORKDIR /app

# Sao chép các file yêu cầu vào container
COPY requirements.txt requirements.txt

# Cài đặt các gói yêu cầu
RUN pip install -r requirements.txt

# Sao chép toàn bộ mã nguồn vào container
COPY . .

# Thiết lập biến môi trường
ENV PYTHONUNBUFFERED=1

# Chạy lệnh để khởi động ứng dụng
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
