# RAG Evals

## Overview

RAGEvals is a Python library for evaluating Retrieval-Augmented Generation (RAG) systems. It provides various metrics to evaluate the quality of generated text against reference text.

## Installation

You can install the library using pip:

```bash
pip install ragevals
```

## Usage

Here's how to use the RAGevals library:

```python
from ragevals import RAGevals

# Initialize the evaluator
evaluator = RAGevals()

# Input data
question = "What are the causes of climate change?"
response = "Climate change is caused by human activities."
reference = "Human activities such as burning fossil fuels cause climate change."


# Evaluate the response
metrics = evaluator.evaluate_all(question, response, reference)

# Print the results
print(metrics)

# Get both metric and description
for metric,result in metrics.items():
  print(f"{metric}: {result['score']:.2f} \n{result['description']}")

```



## Metrics

The following metrics are provided by the library:

- **BLEU**: Measures the overlap between the generated output and reference text based on n-grams.
- **ROUGE-1**: Measures the overlap of unigrams between the generated output and reference text.
- **BERT Score**: Evaluates the semantic similarity between the generated output and reference text using BERT embeddings.
- **Perplexity**: Measures how well a language model predicts the text.
- **Diversity**: Measures the uniqueness of bigrams in the generated output.
- **Racial Bias**: Detects the presence of biased language in the generated output.

## Testing

To run the tests, use the following command:

```
python -m unittest discover -s RAGevals -p "test_*.py"
```
## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! If you have any improvements, suggestions, or bug fixes, feel free to create a pull request (PR) or open an issue on GitHub. Please ensure your contributions adhere to the project's coding standards and include appropriate tests.

### How to Contribute

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes.
4. Run tests to ensure everything is working.
5. Commit your changes and push to your fork.
6. Create a pull request (PR) with a detailed description of your changes.

## Contact

If you have any questions or need further assistance, feel free to reach out via [email](mailto:mailmenaveed88@gmail.com).
