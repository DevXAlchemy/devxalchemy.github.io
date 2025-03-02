# 🎵 Liked Songs Collector  

**GitHub Repository:** [DevXAlchemy/liked-songs-collector](https://github.com/DevXAlchemy/liked-songs-collector/tree/dev)  

## 📌 Overview  
Liked Songs Collector is a web app that aggregates liked songs from multiple music platforms (Spotify, YouTube Music) into a single interface. It allows users to view all their favorite tracks in one place and enables playlist migration between platforms.  

To optimize API usage and improve performance, the app integrates:  
- **Songlink API** to fetch song metadata across platforms efficiently.  
- **Redis caching** to store API responses, reducing redundant calls and ensuring faster retrieval.  

## ✨ Features  
- 📥 **Fetch Liked Songs** from Spotify & YouTube Music  
- 🔄 **Create Playlists** from Spotify songs in YouTube and vice versa  
- 🔗 **Songlink API Integration** to map songs across platforms  
- 🎛 **Simple UI** for easy interaction  
- 🚀 **Future Enhancements:** More platform integrations  

## 🛠 Tech Stack  
- **Frontend:** React (UI)  
- **Backend:** Python (FastAPI)  
- **Database & Caching:** Redis  
- **APIs Used:**  
  - Spotify API  
  - YouTube Music API  
  - Songlink API (Odesli)

## 📂 Project Structure  
```bash
liked-songs-collector/
│── frontend/        # React UI
│── backend/         # FastAPI backend
│── redis/           # Redis caching setup
│── README.md        # Project documentation
│── requirements.txt # Python dependencies
└── .gitignore       # Ignored files
```

## 🚀 Getting Started  

### 1️⃣ Clone the Repository  
```bash
git clone https://github.com/DevXAlchemy/liked-songs-collector.git
cd liked-songs-collector
```

### 2️⃣ Backend Setup  
```bash
cd backend
pip install -r requirements.txt
python app.py  # Start FastAPI backend
```

### 3️⃣ Frontend Setup  
```bash
cd frontend
npm install
npm start  # Start React frontend
```

### 4️⃣ Start Redis Server  
```bash
docker run -d --name redis-cache -p 6379:6379 redis
```

## 🔑 API & Redis Configuration  
- Obtain **Spotify API credentials** from [Spotify Developer Portal](https://developer.spotify.com/)  
- Get **YouTube API key** from [Google Cloud Console](https://console.cloud.google.com/)  
- Store credentials in `.env` files for security  
- **Redis is used for caching song lists and API responses** to improve speed and reduce API costs  

## ⚡ Optimizations  
✅ **Redis Caching:** Speeds up song retrieval by reducing redundant API calls  
✅ **Songlink API:** Eliminates the need for multiple API calls to fetch cross-platform song data  
✅ **Efficient API Calls:** Only fetch new data when necessary  

## 🏗 Future Plans  
✅ Add Apple Music support  
✅ Improve UI/UX  
✅ Enhance playlist sync automation  
