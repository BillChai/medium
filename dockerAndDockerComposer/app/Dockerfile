# 使用官方的 Python 映像作為基礎
FROM python:3.10-slim

# 設置工作目錄
WORKDIR /app

# 複製應用代碼和依賴文件到容器
COPY requirements.txt requirements.txt
COPY app.py app.py

# 安裝依賴
RUN pip install --no-cache-dir -r requirements.txt

# 暴露應用端口
EXPOSE 5000

# 設置容器啟動命令
CMD ["python3", "app.py"]

