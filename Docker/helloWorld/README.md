# Build the image
sudo docker build -t fastapi-hello .

# Run the container
sudo docker run -d -p 8000:8000 fastapi-hello

Then open your browser to 👉 http://localhost:8000

You’ll see:
```
{"message": "Hello, World!"}
```



# If you want to use streamlit

# Build image
docker build -t streamlit-hello .

# Run container
docker run -d -p 8501:8501 streamlit-hello
