# Bot 24/7 AFK

Bot chạy độc lập 24/7 trên hosting, vẫn hoạt động khi đóng web hoặc tab trình duyệt.

## Cài đặt

```bash
npm install
```

## Chạy

```bash
npm start
```

## Kiểm tra trạng thái

Truy cập: `http://localhost:3000/health`

## Deploy lên Hosting

### Cách 1: Render (Miễn phí)
1. Đăng ký tại https://render.com
2. Connect GitHub repo này
3. Chọn "New Web Service"
4. Build command: `npm install`
5. Start command: `npm start`
6. Deploy ✅

### Cách 2: Railway (Miễn phí)
1. Đăng ký tại https://railway.app
2. Connect GitHub
3. Chọn repo này
4. Tự động detect Node.js
5. Deploy ✅

### Cách 3: Replit (Miễn phí)
1. Import repo từ GitHub
2. Click Run
3. Chạy luôn ✅

## Giữ Bot Sống 24/7

- Dùng **UptimeRobot** (miễn phí) để ping `/health` mỗi 5 phút
- Điều này ngăn hosting "sleep" bot của bạn
- Link UptimeRobot: https://uptimerobot.com

## Chạy Trên Máy (Terminal Đóng vẫn chạy)

```bash
npm install -g pm2
pm2 start index.js --name bot-afk
pm2 save
pm2 startup
```

Sau đó bot sẽ chạy khi khởi động lại máy!
