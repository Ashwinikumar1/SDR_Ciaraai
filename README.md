## Run it Locally  
1. Clone the repo

2. Change directory to AIUI
```bash
cd AIUI
```
3. Build Docker image
```bash
docker build -t aiui .
``` 
or if on arm64 architecture (including Apple Silicon): 
```bash
docker buildx build --platform linux/arm64 -t aiui .
```
4. Create Docker container from image
```bash
docker run -d -e OPENAI_API_KEY=<YOUR_API_KEY> -e TTS_PROVIDER=EDGETTS -e EDGETTS_VOICE=en-US-EricNeural -p 8000:80 aiui
```
5. Navigate to `localhost:8000` in a modern browser

