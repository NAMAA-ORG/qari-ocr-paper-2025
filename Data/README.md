# QARI v0.3 Markdown Mixed Dataset

## 📋 Dataset Summary

The QARI v0.3 Markdown Mixed Dataset is a specialized synthetic dataset designed for training Arabic OCR models with a focus on complex document layouts and HTML structure understanding. This dataset is part of the QARI-OCR project, which achieves state-of-the-art performance in Arabic text recognition.

This dataset contains 37,000 synthetically generated Arabic document images (29.6k train, 3.7k validation, 3.7k test) with corresponding ground truth text in HTML/Markdown format, featuring:

- 🔤 Full diacritical marks (tashkeel) support
- 📝 Mixed font sizes within documents (headers, body text, annotations)
- 🎨 12 distinct Arabic fonts ranging from common Naskh to ornate calligraphic styles
- 📄 Realistic document layouts with structural HTML tags
- 🖼️ Multiple text sources including Basma2423 and YoussefAnwar Arabic news

## 🎯 Intended Use

This dataset is specifically designed for:

- Training OCR models that need to understand document structure
- Fine-tuning vision-language models for Arabic text recognition
- Developing systems that preserve formatting and layout information
- Research in Arabic document analysis and understanding

## 📊 Dataset Statistics

| Metric | Value |
|--------|-------|
| Total Images | 37,000 |
| Train Set | 29,600 (80%) |
| Validation Set | 3,700 (10%) |
| Test Set | 3,700 (10%) |
| Font Variety | 12 Arabic fonts |
| Font Size Range | 14px - 100px |
| Diacritics Support | ✅ Full tashkeel |
| HTML Structure | ✅ Preserved |
| Layout Complexity | ✅ High (mixed sizes, headers) |

## 🔧 Data Generation Pipeline

| Stage | Process | Details |
|-------|---------|---------|
| 1. Text Collection | Source gathering | Basma2423 (with diacritics) + YoussefAnwar Arabic news |
| 2. HTML Templating | Layout generation | Mixed font sizes, structural elements |
| 3. Rendering | WeasyPrint → PDF → Image | High-quality document rendering |
| 4. Degradation | Synthetic noise | Clean / Moderate / Heavy variants |

## 📈 Model Performance

When used to train QARI v0.3, this dataset enables:

| Metric | Score |
|--------|-------|
| Character Error Rate (CER) | 0.300 |
| Word Error Rate (WER) | 0.485 |
| BLEU Score | 0.545 |
| Training Time | 11 hours |
| CO₂ Emissions | 1.88 kg eq. |

### Key Advantages:

- 📐 Superior layout understanding compared to plain text models
- 🏷️ HTML tag preservation for structured document conversion
- ⚡ Resource efficient - 5x less training time than larger datasets
- 🎯 Specialized performance for document structure tasks

## 📁 Dataset Files

- `train-00000-of-00001-3.parquet` - Training set (29,600 samples)
- `validation-00000-of-00001.parquet` - Validation set (3,700 samples)
- `test-00000-of-00001-2.parquet` - Test set (3,700 samples)
- `samples.json` - Sample dataset with 100 anonymized examples

## 📝 Data Format

Each sample in the dataset contains:
- `image`: Document image (PNG format, base64 encoded in JSON samples)
- `text`: Ground truth text in HTML/Markdown format with full diacritics
- `source`: Original text source (removed in anonymized samples)


## 📄 License

Please refer to the main project repository for licensing information.
