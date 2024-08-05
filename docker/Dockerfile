# Sử dụng hình ảnh cơ bản của Python
FROM python:3.9-slim

# Thiết lập thư mục làm việc
WORKDIR /app

# Sao chép toàn bộ mã nguồn vào container
COPY . .

# In ra danh sách file trong thư mục /app để kiểm tra
RUN ls -la /app

# Thiết lập biến môi trường
ENV PYTHONUNBUFFERED=1

# Cài đặt các gói yêu cầu từ requirements.txt (nếu có)
RUN if [ -f requirements.txt ]; then pip install -r requirements.txt; fi

# Chạy lệnh để khởi động ứng dụng
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
