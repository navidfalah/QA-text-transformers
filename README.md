# 🐍 Question Answering with Transformers

## 📝 Description
This Python script demonstrates how to build a **Question Answering (QA) system** using transformer models. It leverages the `transformers` library by Hugging Face and integrates with **Elasticsearch** for document retrieval. The script includes data preprocessing, model inference, and evaluation on the SubjQA dataset. 🛠️

---

## 🛠️ Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/navidfalah/qa-transformers.git
   cd qa-transformers
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Install additional libraries:
   ```bash
   pip install datasets farm-haystack[colab] elasticsearch
   ```

4. Set up Elasticsearch:
   ```bash
   wget -nc -q https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-7.9.2-linux-x86_64.tar.gz
   tar -xzf elasticsearch-7.9.2-linux-x86_64.tar.gz
   chown -R daemon:daemon elasticsearch-7.9.2
   ```

5. Start Elasticsearch:
   ```bash
   elasticsearch-7.9.2/bin/elasticsearch
   ```

---

## 🚀 Usage

1. Run the script:
   ```bash
   python qa_transformers.py
   ```

2. The script will:
   - Load the SubjQA dataset for electronics-related questions.
   - Preprocess the data and tokenize questions and contexts.
   - Use a pre-trained MiniLM model for question answering.
   - Integrate with Elasticsearch for document retrieval.
   - Perform QA inference and display answers.

---

## 📂 File Structure

```
qa-transformers/
├── qa_transformers.py  # Main script
├── README.md           # This file
├── requirements.txt    # Dependencies
└── data/               # (Optional) Data folder for local datasets
```

---

## 🧩 Key Features

- **Question Answering**:
  - Use a pre-trained MiniLM model (`deepset/minilm-uncased-squad2`) for QA tasks.
  - Handle both answerable and unanswerable questions.

- **Elasticsearch Integration**:
  - Set up Elasticsearch for document retrieval.
  - Store and retrieve document embeddings for dense retrieval.

- **Data Preprocessing**:
  - Tokenize questions and contexts using Hugging Face's `AutoTokenizer`.
  - Handle long contexts with sliding windows and stride.

- **Visualization**:
  - Plot the frequency of question types (e.g., "What", "How", "Is").

---

## 📊 Example Outputs

1. **Question Types**:
   - Bar chart showing the frequency of question types in the dataset.

2. **QA Inference**:
   - Example question: "How much music can this hold?"
   - Example answer: "6000 hours"

3. **Elasticsearch Setup**:
   - Confirmation of Elasticsearch running on `localhost:9200`.

---

## 🤖 Models Used

- **MiniLM**: A pre-trained transformer model fine-tuned on SQuAD 2.0 for question answering.
- **Elasticsearch**: For document storage and retrieval.

---

## 📈 Performance Metrics

- **Answer Accuracy**: Evaluated on the SubjQA dataset.
- **Retrieval Speed**: Measured using Elasticsearch.

---

## 🛠️ Dependencies

- Python 3.x
- Libraries:
  - `transformers`, `datasets`, `farm-haystack`
  - `elasticsearch`, `torch`, `matplotlib`
  - `pandas`, `numpy`

---

## 🤝 Contributing

Contributions are welcome! 🎉 Feel free to open an issue or submit a pull request.

1. Fork the repository.
2. Create a new branch: `git checkout -b feature/your-feature`.
3. Commit your changes: `git commit -m "Add your feature"`.
4. Push to the branch: `git push origin feature/your-feature`.
5. Open a pull request.

---

## 📜 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- Hugging Face for the `transformers` library.
- Elastic for Elasticsearch.
- The SubjQA dataset for providing the QA evaluation data.

---

## 👤 Author

- **Name**: Navid Falah
- **GitHub**: [navidfalah](https://github.com/navidfalah)
- **Email**: navid.falah7@gmail.com
