# 🕷️ Crawl4AI Project

A smart content crawler designed to extract clean, structured, and LLM-ready markdown files from websites using the powerful Crawl4AI library.

## 🚀 Overview

This project provides an intelligent web scraping solution that converts website content into clean, structured markdown files optimized for Large Language Models (LLMs) and documentation purposes.

## ✨ Features

- **Sitemap Crawling**: Automatically discover and crawl pages from XML sitemaps
- **URL-based Crawling**: Crawl specific URLs or website sections
- **Markdown Output**: Clean, structured markdown files ready for documentation
- **Content Filtering**: Advanced filtering based on:
  - Word count thresholds
  - Image ratio analysis  
  - Link density evaluation
- **CLI Interface**: Easy-to-use command-line interface
- **Async Processing**: High-performance asynchronous crawling
- **Progress Tracking**: Real-time progress monitoring with tqdm

## 🛠️ Tech Stack

- **Python 3.x**
- **Crawl4AI**: Core crawling engine
- **aiohttp**: Asynchronous HTTP client
- **tqdm**: Progress bar visualization
- **psutil**: System resource monitoring

## 📦 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/jerops/crawl4ai-project.git
   cd crawl4ai-project
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

## 🧠 Usage

### Basic Sitemap Crawling
```bash
python crawl_and_publish.py --sitemap https://example.com/sitemap.xml --output docs/
```

### Advanced Options
```bash
python crawl_and_publish.py \
    --sitemap https://example.com/sitemap.xml \
    --output ./extracted_content/ \
    --min-words 100 \
    --max-image-ratio 0.3 \
    --max-link-density 0.5
```

### Single URL Crawling
```bash
python crawl_and_publish.py \
    --url https://example.com/specific-page \
    --output ./single_page/
```

## ⚙️ Configuration

The crawler supports various configuration options for content filtering:

- `--min-words`: Minimum word count for page inclusion
- `--max-image-ratio`: Maximum ratio of images to content
- `--max-link-density`: Maximum density of links in content
- `--output`: Output directory for markdown files

## 📁 Output Structure

The crawler organizes extracted content in a structured format:

```
output_directory/
├── page-title-1.md
├── page-title-2.md
├── category/
│   ├── subcategory-page.md
│   └── another-page.md
└── index.md
```

## 🎯 Use Cases

- **Documentation Generation**: Convert websites to structured documentation
- **Content Migration**: Extract content for site migrations
- **LLM Training Data**: Prepare clean text for language model training
- **Content Analysis**: Analyze website structure and content quality
- **SEO Auditing**: Extract content for SEO analysis

## 🤝 Contributing

Contributions are welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🔗 Dependencies

See [requirements.txt](requirements.txt) for the complete list of Python dependencies.

---

**Author**: [Jerops](https://github.com/jerops)  
**Keywords**: web-scraping, crawl4ai, markdown, llm, content-extraction, python