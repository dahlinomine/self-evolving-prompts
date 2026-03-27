# Self-Evolving Prompts

![optimization](https://img.shields.io/badge/optimization-blue?style=flat-square) ![prompt-engineering](https://img.shields.io/badge/prompt--engineering-blue?style=flat-square) ![meta](https://img.shields.io/badge/meta-blue?style=flat-square)

A framework for agents to run A/B tests on their own system prompts for accuracy.

## Overview
Self-Evolving Prompts is a meta-optimization framework designed to help LLM agents iteratively improve their own performance. By treating system instructions as variables, the framework allows agents to conduct automated A/B tests, evaluate response accuracy against defined metrics, and self-select the most effective prompt iterations.

## Features
*   **Automated A/B Testing:** Seamlessly swap and compare multiple system prompt variations in real-time.
*   **Performance Analytics:** Built-in scoring mechanisms to evaluate prompt accuracy based on custom success criteria.
*   **Evolutionary Loops:** Automatically promotes high-performing prompts while phasing out inefficient instructions.
*   **Environment Agnostic:** Easily integrates with various LLM providers and existing agentic workflows.

## Installation
Clone the repository and install the necessary dependencies using pip:

```bash
git clone https://github.com/username/self-evolving-prompts.git
cd self-evolving-prompts
pip install -r requirements.txt
```

## Usage
To start the evolution process, configure your base prompt and target metrics, then run the main entry point:

```bash
python main.py
```

**Example:**
```python
from engine import PromptEvolver

# Initialize the evolver with a base objective
evolver = PromptEvolver(
    base_prompt="You are a precise technical assistant.",
    iterations=10
)

# Run the A/B testing suite
best_prompt = evolver.evolve()
print(f"Optimized Prompt: {best_prompt}")
```

## Contributing
Contributions are welcome! If you have suggestions for new evolution strategies or performance metrics, please open an issue or submit a pull request. Ensure all code adheres to the existing style guidelines and include tests for new functionality.

## License
This project is licensed under the [MIT License](LICENSE).