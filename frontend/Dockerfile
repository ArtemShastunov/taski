# Базовый образ с Node.js (Alpine — лёгкая версия)
FROM node:18-alpine

# Рабочая директория
WORKDIR /app

# Копируем package.json и устанавливаем зависимости
COPY package*.json ./
RUN npm install

# Копируем исходный код
COPY . .

# Собираем продакшн-версию (создаст папку /app/build)
RUN npm run build

# CMD будет переопределён в docker-compose.yml, но пусть будет на всякий случай
CMD ["npm", "start"]