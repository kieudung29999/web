# Sử dụng image Node.js
FROM node:14

# Thiết lập thư mục làm việc trong container
WORKDIR /app

# Sao chép file package.json và package-lock.json
COPY package*.json ./

# Cài đặt các dependencies
RUN npm install

# Sao chép mã nguồn của ứng dụng vào container
COPY . .

# Cấp quyền truy cập cổng 3000
EXPOSE 3000
m
