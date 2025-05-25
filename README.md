# 🧠 MCP Server(Model Control Protocol)

A modular FastAPI backend designed for controlling and automating the lifecycle of quote generation, image handling, video metadata management, and structured content distribution — powered by PostgreSQL and modern Python tooling.

---

## 🚀 Features

- 🔡 **Quotes & Structure Generator**
- 🖼️ **Image Downloader, Resizer & ALT Text Matcher**
- 🔄 **Batch Submit to Azure OpenAI**
- 📹 **Video Metadata Cleaner**
- 📊 **Metadata Generator & Textual Merge**
- 🧭 **Circular Navigation Logic for Stories**
- 🧹 **Final Quote Fancy Data Reordering**
- 📥 **All data handled via PostgreSQL**

---

## 📦 Folder Structure

MCP_SERVER/
├── main.py                  # FastAPI entry point
├── .env                     # Environment secrets (PG_HOST, PG_USER, etc.)
├── routers/                 # All feature routes modularized
│   ├── quotes.py
│   ├── image_router.py
│   ├── altxt.py
│   ├── rotate.py
│   ├── reorder.py
│   └── …
├── requirements.txt         # All dependencies


---

## 🛠️ Setup & Run Locally

### 1. Clone the repository

```bash
git clone https://github.com/Iamkrmayank/quote-fancy-mcp-server.git
cd mcp-server
```
### 2. Create .env file

```
PG_HOST=localhost
PG_PORT=5432
PG_DATABASE=your_db
PG_USER=your_user
PG_PASSWORD=your_password
```

### 3. Install dependencies
```
pip install -r requirements.txt
```
### 4. Run the FastAPI server
```
uvicorn main:app --reload
```

### 5. Key Endpoints

## 🔁 Key Endpoints

| Method | Endpoint             | Description                                      |
|--------|----------------------|--------------------------------------------------|
| POST   | `/quotes/`           | Generate or scrape quotes                        |
| POST   | `/generate/`         | Generate structured textual content              |
| POST   | `/images/`           | Download images from external sources            |
| POST   | `/match/`            | Match ALT text with images                       |
| POST   | `/azure/`            | Submit batch text tasks to Azure OpenAI          |
| POST   | `/track/`            | Track Azure batch image processing               |
| POST   | `/merge_text/`       | Merge structured quote content                   |
| POST   | `/resizer/`          | Resize and save images to S3/CDN                 |
| POST   | `/distribute/`       | Distribute image URLs and paragraph text         |
| POST   | `/videometa/`        | Clean and normalize video metadata               |
| POST   | `/modify_column/`    | Remove or update specific DB columns             |
| POST   | `/metadata/`         | Generate metadata (title, description, keywords) |
| POST   | `/rotate/`           | Add circular next/prev navigation to stories     |
| POST   | `/reorder/`          | Reorder final output to `final_quote_fancy_data` |

📍 Access Swagger UI: [http://localhost:8000/docs](http://localhost:8000/docs)

📄 License

MIT License


👨‍💻 Author

Kumar Mayank
📬 LinkedIn
🌐 GitHub
