# Uploading Large Files to AWS S3 with Lightning-Fast Speed - Parallel Chunk Upload

Demonstrates two approaches for lightning-fast large file uploads to AWS S3 via chunking and parallelization. One approach uses frontend chunk creation with the AWS multipart API, while the other creates chunks on the backend using AWS SDK v3’s parallel upload technique. By splitting files into chunks and uploading them simultaneously, transfer times are minimized, and upload reliability is improved.

## Techniques Overview

### **Technique 1: Frontend Chunk Creation & AWS Multipart Upload API**

In this approach, files are divided into chunks on the frontend, then sent to the backend, which utilizes AWS S3’s multipart upload API for efficient processing.

#### **Backend Setup**

- **Folder:** `backend`
- Install dependencies:
  ```bash
  npm install
  ```
- Create a `.env` file by copying `sample.env` and updating the required values.
- Start the backend server:
  ```bash
  npm start
  ```

#### **Frontend Setup**

- **Folder:** `frontend`
- Install `http-server` globally:
  ```bash
  npm install -g http-server
  ```
- Navigate to the `frontend` directory.
- Start the frontend server:
  ```bash
  http-server
  ```
- Open the provided URL in your web browser.

---

### **Technique 2: Backend Chunk Creation & Parallel Upload with AWS SDK v3**

In this approach, the entire file is first uploaded to the backend, where it is divided into chunks and uploaded to S3 in parallel using AWS SDK v3’s managed uploader.

#### **Backend Setup**

- **Folder:** `backend2`
- Install dependencies:
  ```bash
  npm install
  ```
- Create a `.env` file by copying `sample.env` and updating the necessary values.
- Start the backend server:
  ```bash
  npm start
  ```

#### **Frontend Setup**

- **Folder:** `frontend2`
- Install `http-server` globally:
  ```bash
  npm install -g http-server
  ```
- Navigate to the `frontend2` directory.
- Start the frontend server:
  ```bash
  http-server
  ```
- Open the provided URL in your web browser.


