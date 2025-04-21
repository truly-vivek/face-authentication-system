# Face Authentication System

A complete face recognition system with registration, login, and live recognition capabilities using face-api.js.

![System Demo](demo.gif) <!-- Add a demo gif if available -->

## Features

- 👤 User registration with facial recognition  
- 🔐 Secure face-based login  
- 👀 Real-time live face recognition  
- 🏠 Welcome dashboard  
- 📱 Responsive design for all devices  

## Technologies Used

- **Frontend**: HTML5, CSS3, JavaScript  
- **Face Recognition**: [face-api.js](https://github.com/justadudewhohacks/face-api.js)  
- **Browser APIs**: MediaDevices, Canvas, LocalStorage  

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/face-authentication-system.git
   cd face-authentication-system
   ```

2. Download face-api.js models:
   ```bash
   mkdir models
   cd models
   wget https://github.com/justadudewhohacks/face-api.js/raw/master/models/age_gender_model-shard1
   wget https://github.com/justadudewhohacks/face-api.js/raw/master/models/age_gender_model-weights_manifest.json
   wget https://github.com/justadudewhohacks/face-api.js/raw/master/models/face_landmark_68_model-shard1
   wget https://github.com/justadudewhohacks/face-api.js/raw/master/models/face_landmark_68_model-weights_manifest.json
   wget https://github.com/justadudewhohacks/face-api.js/raw/master/models/face_recognition_model-shard1
   wget https://github.com/justadudewhohacks/face-api.js/raw/master/models/face_recognition_model-shard2
   wget https://github.com/justadudewhohacks/face-api.js/raw/master/models/face_recognition_model-weights_manifest.json
   wget https://github.com/justadudewhohacks/face-api.js/raw/master/models/tiny_face_detector_model-shard1
   wget https://github.com/justadudewhohacks/face-api.js/raw/master/models/tiny_face_detector_model-weights_manifest.json
   ```

3. Serve the application:
   - Using Python:
     ```bash
     python3 -m http.server 8000
     ```
   - Or install `http-server`:
     ```bash
     npm install -g http-server
     http-server -p 8000
     ```

4. Open in browser:
   ```
   http://localhost:8000
   ```

## File Structure

```
face-authentication-system/
│
├── index.html          # Welcome page
├── register.html       # User registration
├── login.html          # User login
├── live.html           # Live recognition
├── dashboard.html      # User dashboard
│
├── models/             # face-api.js models
│   ├── tiny_face_detector_model-*
│   ├── face_landmark_68_model-*
│   └── face_recognition_model-*
│
├── README.md           # This file
└── demo.gif            # System demo (optional)
```

## Usage Guide

### 1. Registration
- Click "Register" on the welcome page  
- Enter your username  
- Position your face clearly in the camera view  
- Click "Capture Face" to register your facial data  

### 2. Login
- Click "Login" on the welcome page  
- Look at the camera to authenticate  
- You'll be redirected to dashboard upon successful recognition  

### 3. Live Recognition
- Access the live recognition page  
- The system will continuously scan and identify registered users  
- Recognized faces appear with name and confidence level  

## Configuration Options

In `live.html`, you can adjust these parameters:

```javascript
// Recognition sensitivity (lower = more strict)
const MATCH_THRESHOLD = 0.6;

// Detection interval in milliseconds
const RECOGNITION_INTERVAL = 800;

// Face detection options
const detectionOptions = new faceapi.TinyFaceDetectorOptions({
  inputSize: 320,       // Higher = more accurate but slower
  scoreThreshold: 0.5   // Minimum confidence for face detection
});
```

## Troubleshooting

**Issue**: Camera not working  
- Verify browser permissions  
- Ensure no other application is using the camera  
- Try a different browser (Chrome recommended)  

**Issue**: Models not loading  
- Check console for errors  
- Verify models are in the `/models` directory  
- Ensure you're running from a web server (not file://)  

**Issue**: Poor recognition accuracy  
- Register in good lighting conditions  
- Try different angles during registration  
- Adjust `MATCH_THRESHOLD` in the code  

## Browser Support

- Chrome (recommended)  
- Firefox  
- Edge  
- Safari (limited support)  

Note: Requires modern browser with WebGL and WebRTC support.

## Future Enhancements

- [ ] Add backend server for user management  
- [ ] Implement multi-factor authentication  
- [ ] Add liveness detection  
- [ ] Support for multiple faces in frame  
- [ ] Admin dashboard for user management  

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository  
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)  
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)  
4. Push to the branch (`git push origin feature/AmazingFeature`)  
5. Open a Pull Request  

## License

Distributed under the MIT License. See `LICENSE` for more information.

## Contact

Vivek - [@truly_vivek](mailto:vivekreddykesavarapu@gmail.com) 

Project Link: [https://github.com/your-username/face-authentication-system](https://github.com/your-username/face-authentication-system)