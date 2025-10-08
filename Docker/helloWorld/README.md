# Build the image
sudo docker build -t fastapi-hello .

# Run the container
sudo docker run -d -p 8000:8000 fastapi-hello

Then open your browser to 👉 http://localhost:8000

You’ll see:
```
{"message": "Hello, World!"}
```