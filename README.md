# Movie Metadata Scraper

A lightweight, efficient CLI tool designed to fetch comprehensive movie metadata using the **TMDB (The Movie Database) API**. This tool is perfect for media server enthusiasts (Plex/Jellyfin) or data scientists looking to build movie datasets.

## 🚀 Features

* **Batch Processing:** Scrape metadata for a list of movie titles from a CSV or Text file.
* **Rich Metadata:** Extracts titles, release dates, genres, runtime, budget, revenue, and high-res poster URLs.
* **Search Optimization:** Uses fuzzy matching to ensure the correct movie is found even with minor typos.
* **Export Formats:** Save results to `.json` or `.csv`.
* **Rate Limit Handling:** Built-in "sleep" logic to respect TMDB API limits.

---

## 🛠️ Installation

1. **Clone the repository:**
```bash
git clone https://github.com/yourusername/movie-metadata-scraper.git
cd movie-metadata-scraper

```


2. **Create a virtual environment (optional but recommended):**
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

```


3. **Install dependencies:**
```bash
pip install -r requirements.txt

```



---

## 🔑 API Configuration

To use this tool, you must have a TMDB API Key (v3 auth).

1. Sign up for an account at [themoviedb.org](https://www.themoviedb.org/).
2. Navigate to your account settings and request an API key.
3. Create a `.env` file in the root directory of this project:
```bash
touch .env

```


4. Add your token to the `.env` file:
```env
TMDB_API_KEY=your_api_key_here_xxxxxx

```



---

## 📖 Usage

### Basic Search

Scrape data for a single movie directly from the terminal:

```bash
python main.py --search "Inception"

```

### Batch Processing

Point the script to a file containing a list of movie titles (one per line):

```bash
python main.py --input movies.txt --output data.json

```

### Arguments

| Argument | Description | Default |
| --- | --- | --- |
| `--search` | Single movie title to search for | None |
| `--input` | Path to input file (.txt or .csv) | None |
| `--output` | Path for the output file | `results.json` |
| `--format` | Output format (`json` or `csv`) | `json` |

---

## 📂 Project Structure

```text
movie-metadata-scraper/
├── src/
│   ├── scraper.py       # Core API logic
│   ├── utils.py         # File handling and formatting
│   └── config.py        # Environment variable loader
├── main.py              # CLI Entry point
├── .env                 # API Keys (gitignored)
├── requirements.txt     # Project dependencies
└── README.md

```

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

## 📝 License

Distributed under the MIT License. See `LICENSE` for more information.

---

**Disclaimer:** This project is not affiliated with, maintained, authorized, endorsed, or sponsored by The Movie Database (TMDB).
