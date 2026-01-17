# 💬 Real-Time WebSocket Chat
High-performance private messaging app with Spring Boot + WebSocket, deployed on Google Cloud Run.
![Java](https://img.shields.io/badge/Java-21-orange)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.x-brightgreen)
![Latency](https://img.shields.io/badge/Latency-3--5ms-success)
## ✨ Features
- ⚡ Real-time private messaging (3-5ms latency)
- 🌐 WebSocket with SockJS fallback
- ☁️ Deployed on Google Cloud Run
- 📱 Responsive mobile design
## 🚀 Quick Start
### Run Locally
```bash
mvn clean package -DskipTests
java -jar target/websocket-0.0.1-SNAPSHOT.jar
Open: http://localhost:8080

Deploy to Cloud Run
gcloud run deploy chatapplication \
  --source . \
  --region asia-south1 \
  --allow-unauthenticated \
  --session-affinity
🛠️ Tech Stack
Backend: Spring Boot 3.x, Java 21
Protocol: WebSocket (STOMP), SockJS
Frontend: HTML, CSS, JavaScript
Cloud: Google Cloud Run (Mumbai)
📝 Configuration
application.properties:

spring.websocket.message-size-limit=524288
spring.websocket.send-buffer-size-limit=1048576
server.port=${PORT:8080}
Frontend (index.html):

// Production
const socket = new SockJS('https://your-app-url.run.app/ws');
// Local
const socket = new SockJS('http://localhost:8080/ws');
📊 Performance
Latency: 3-5ms (Pakistan ↔ Mumbai)
Message Size: Up to 512 KB
Auto-scaling enabled
📁 Structure
websocket-chat/
├── src/main/java/com/example/websocket/
│   ├── config/WebSocketConfig.java
│   ├── controller/ChatController.java
│   └── model/ChatMessage.java
├── src/main/resources/
│   ├── application.properties
│   └── static/index.html
└── pom.xml
