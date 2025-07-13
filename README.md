# 🧳 旅遊小助手 Travel Assistant

一個基於 Vue.js + Spring Boot + PostgreSQL 的智慧旅遊行程規劃系統，幫助使用者輕鬆規劃完美旅程。

## 📋 目錄

- [功能特色](#-功能特色)
- [技術架構](#-技術架構)
- [專案結構](#-專案結構)
- [快速開始](#-快速開始)
- [API 文件](#-api-文件)
- [開發指南](#-開發指南)

## ✨ 功能特色

### 🎯 核心功能
- **智慧行程規劃**：輸入出發地、目的地、日期，系統自動推薦景點
- **行程管理**：建立、查看、搜尋、刪除旅遊行程
- **景點推薦**：根據目的地提供當地熱門景點建議
- **資料持久化**：所有行程資料安全儲存在 PostgreSQL 資料庫

### 🛠️ 技術特色
- **現代化前端**：Vue 3 + Vite + Element Plus，響應式設計
- **強健後端**：Spring Boot + JPA + PostgreSQL，RESTful API
- **完整文件**：Swagger UI 提供互動式 API 文件
- **容器化部署**：Docker + Docker Compose 一鍵部署
- **開發友好**：熱重載、自動建構、詳細日誌

## 🏗️ 技術架構

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Vue.js 前端    │    │ Spring Boot 後端 │    │ PostgreSQL 資料庫│
│                 │    │                 │    │                 │
│ • Vue 3         │◄──►│ • RESTful API   │◄──►│ • 行程資料表     │
│ • Vite          │    │ • JPA/Hibernate │    │ • 索引優化       │
│ • Element Plus  │    │ • Swagger UI    │    │ • 自動備份       │
│ • Axios         │    │ • 資料驗證       │    │                 │
└─────────────────┘    └─────────────────┘    └─────────────────┘
         │                       │                       │
         └───────────────────────┼───────────────────────┘
                                 │
                    ┌─────────────────┐
                    │ Docker Compose  │
                    │                 │
                    │ • 容器編排       │
                    │ • 網路配置       │
                    │ • 資料卷管理     │
                    └─────────────────┘
```

## 📁 專案結構

```
mytravel/
├── backend/                    # Spring Boot 後端
│   ├── src/main/java/com/mytravel/
│   │   ├── TravelAssistantApplication.java
│   │   ├── controller/         # REST 控制器
│   │   ├── service/           # 業務邏輯層
│   │   ├── repository/        # 資料存取層
│   │   ├── entity/           # JPA 實體類別
│   │   ├── dto/              # 資料傳輸物件
│   │   └── config/           # 配置類別
│   ├── src/main/resources/
│   │   └── application.yml    # 應用程式配置
│   ├── pom.xml               # Maven 依賴配置
│   └── Dockerfile            # 後端容器配置
├── frontend/                  # Vue.js 前端
│   ├── src/
│   │   ├── components/       # Vue 元件
│   │   ├── views/           # 頁面元件
│   │   ├── router/          # 路由配置
│   │   ├── api/             # API 服務
│   │   └── main.js          # 應用程式進入點
│   ├── package.json         # NPM 依賴配置
│   ├── vite.config.js       # Vite 建構配置
│   ├── nginx.conf           # Nginx 配置
│   └── Dockerfile           # 前端容器配置
├── db/
│   └── schema.sql           # 資料庫初始化腳本
├── docker-compose.yml       # Docker 編排配置
└── README.md               # 專案說明文件
```

## 🚀 快速開始

### 1. 下載專案
```bash
# 複製專案
git clone https://github.com/Mark850409/20250713_mytravel.git
cd 20250713_mytravel
```

### 2. 一鍵啟動

#### Windows 使用者：
```bash
start.bat
```

#### macOS/Linux 使用者：
```bash
chmod +x start.sh
./start.sh
```

### 3. 驗證部署
等待約 2-3 分鐘讓所有服務完全啟動，然後訪問：

- **前端應用**: http://localhost:3000
- **後端 API**: http://localhost:8080
- **Swagger UI**: http://localhost:8080/swagger-ui.html
- **pgAdmin 資料庫管理**: http://localhost:5050

## 📚 API 文件

### 主要 API 端點

| 方法 | 端點 | 描述 |
|------|------|------|
| POST | `/api/travel-plans` | 建立新的旅遊行程 |
| GET | `/api/travel-plans` | 取得所有旅遊行程 |
| GET | `/api/travel-plans/{id}` | 取得特定行程詳情 |
| GET | `/api/travel-plans/search` | 搜尋旅遊行程 |
| DELETE | `/api/travel-plans/{id}` | 刪除旅遊行程 |

## 🔧 開發指南

### 後端開發
```bash
cd backend
./mvnw spring-boot:run
```

### 前端開發
```bash
cd frontend
npm install
npm run dev
```

## 📄 授權條款

本專案採用 MIT 授權條款。

---

**🎉 感謝使用旅遊小助手！祝您旅途愉快！**