FROM python:3.9

# Set the working dir in the container
WORKDIR /usr/src/app

# Copy the dependencies file into the working dir
COPY requirements.txt ./

# Install any packages in the req
RUN pip install --no-cache-dir -r requirements.txt

# Copy contents of local src to the working dir
COPY . .

# Run the application
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "80"]