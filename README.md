# 🚀 QuickPrompt [Under Development]

[![PyPI version](https://badge.fury.io/py/quickprompt.svg)](https://badge.fury.io/py/quickprompt)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python Versions](https://img.shields.io/pypi/pyversions/quickprompt.svg)](https://pypi.org/project/quickprompt/)

QuickPrompt is a powerful tool for rapidly generating high-quality prompts for various AI models, tailored to specific use cases and requirements.

## 🌟 Features

- 🧠 Supports multiple LLM providers (OpenAI, Anthropic, Groq)
- 🎯 Generates prompts tailored to specific use cases
- 🔧 Customizable input and output formats
- 🚀 Easy-to-use CLI and Python API
- 🔒 Secure handling of API keys

## 🛠 Installation

Install QuickPrompt using pip:

```bash
pip install quickprompt
```

## 🚀 Quick Start

### Using as a Python Package

```python
from quickprompt import generate_prompt, ModelConfig, SupportedProviders, GroqModels
import os

model_config = ModelConfig(
    SupportedProviders.GROQ,
    GroqModels.LLAMA3_70B.value,
    os.environ.get("GROQ_API_KEY")
)

prompt = generate_prompt(
    model_config=model_config,
    input_type="Text",
    input_format="JSON",
    use_case="Sentiment Analysis",
    output_format="JSON",
    output_type="Classification",
    additional_context={"max_tokens": 100, "temperature": 0.7}
)

print(prompt)
```

### Using the Command Line Interface

```bash
export GROQ_API_KEY=your_groq_api_key
quickprompt groq llama3-70b-8192 "Text" "JSON" "Sentiment Analysis" "JSON" "Classification" --additional_context max_tokens=100 temperature=0.7
```

## 🌐 Supported Models

- OpenAI
- Anthropic
- Groq
  - Llama 3 70B
  - Llama 3 8B
  - Llama 3 8B Tool Use
  - Llama 3.1 70B
  - Llama 3.1 8B
  - Mixtral 8x7B
  - Llama Guard

## 🛠 Development

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/quickprompt.git
   cd quickprompt
   ```

2. Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Install the package in editable mode:
   ```bash
   pip install -e .
   ```

5. Run tests:
   ```bash
   pytest tests/
   ```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgements

- Thanks to all contributors who have helped shape QuickPrompt
- Special thanks to the teams at OpenAI, Anthropic, and Groq for their amazing language models

## 📞 Contact

For any queries or suggestions, please open an issue on GitHub or contact the maintainer at [aj.das.research@gmail.com](mailto:aj.das.research@gmail.com).

---

Made with ❤️ by [Abhijit Das]
