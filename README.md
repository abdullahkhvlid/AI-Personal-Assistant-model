# AI Productivity Planner

An intelligent productivity planning system that uses local AI to generate personalized study schedules and productivity plans. Built with GPT4All and Mistral-7B, this tool creates custom schedules based on your goals, available time, and focus areas.

## Features

- **Personalized Scheduling**: Generates custom daily plans based on your specific goals and available hours
- **AI-Powered Recommendations**: Provides study suggestions, break ideas, and task prioritization
- **Local AI Processing**: Runs entirely offline using GPT4All and Mistral-7B model
- **Interactive Interface**: Simple command-line interface for easy user interaction
- **Smart Summarization**: Automatically creates concise 5-point summaries of generated plans
- **Motivational Content**: Includes AI-generated motivational lines to keep you inspired

## Installation

```bash
pip install gpt4all
```

## Usage

```python
from gpt4all import GPT4All

# Initialize the AI model
model = GPT4All("mistral-7b-instruct-v0.1.Q4_0.gguf")

def ask(prompt):
    return model.generate(prompt, max_tokens=600)

# Get user inputs
name = input("Enter your name: ")
g1 = input("Goal 1: ")
g2 = input("Goal 2: ")
g3 = input("Goal 3: ")
hours = input("Study hours: ")
topic = input("Focus topic: ")

# Generate personalized plan
full_prompt = f"""
Create a personalized productivity plan for a student named {name}.
Goals: {g1}, {g2}, {g3}.
Available study hours: {hours}.
Focus topic: {topic}.
Include time blocks, study suggestions, break ideas, and task priorities.
"""

plan = ask(full_prompt)

# Generate summary
summary_prompt = f"Summarize the following plan in exactly 5 bullet points. Plan: {plan}"
summary = ask(summary_prompt)

# Get motivation
motivation = ask("Give 3 short motivational lines for a student starting their daily routine.")

print("\nPersonalized Schedule\n")
print(plan)
print("\nSummary\n")
print(summary)
print("\nMotivation\n")
print(motivation)
```

## Example Output

```
Personalized Schedule

Task Priorities:
1. Study ML concepts (2 hours)
2. Practice coding exercises (1 hour)
3. Exercise regularly (1 hour)
4. Improve health habits (0.5 hours)

Time Blocks:
- 9am - 11am: Study ML concepts
- 1pm - 2pm: Practice coding exercises
- 6pm - 7pm: Exercise regularly
- 8pm - 8.5 hours: Improve health habits

Study Suggestions:
- Use online resources such as Coursera, edX or Khan Academy
- Take notes and summarize key points for better retention
- Practice solving coding exercises related to ML algorithms

Summary

1. Study ML concepts for 2 hours using online resources
2. Practice coding exercises related to ML algorithms for 1 hour
3. Exercise regularly for 1 hour during the day
4. Improve health habits by taking regular breaks
5. Use Pomodoro technique for focused study sessions

Motivation

1) "Believe in yourself and your abilities, you got this!"
2) Every step you take brings you closer to achieving your goals.
3) Embrace the challenges that come your way, they are opportunities for growth.
```

## How It Works

1. **User Input Collection**: Gathers name, goals, available hours, and focus topic
2. **AI Plan Generation**: Uses Mistral-7B to create a comprehensive productivity plan
3. **Content Processing**: Generates summaries and motivational content
4. **Optional Features**: Provides additional productivity tips on demand

## Model Information

- **Model**: mistral-7b-instruct-v0.1.Q4_0.gguf
- **Size**: 4.11 GB
- **Framework**: GPT4All
- **Operation**: Local/Offline

## Benefits

- **Privacy First**: All processing happens locally, no data sent to cloud services
- **Cost Effective**: No API costs or usage limits
- **Customizable**: Easily adaptable for different planning needs
- **Always Available**: Works offline without internet connection

## Use Cases

- Student study planning
- Professional productivity scheduling
- Personal development planning
- Time management optimization
- Goal achievement tracking

## Requirements

- Python 3.8+
- 8GB+ RAM recommended
- 5GB+ storage for model files
- GPT4All compatible system

## Project Structure

```
ai-productivity-planner/
├── productivity_planner.py
├── requirements.txt
├── README.md
└── examples/
    └── sample_output.txt
```

## Contributing

Feel free to contribute by:
- Adding new planning templates
- Improving the user interface
- Enhancing prompt engineering
- Adding export functionality

## License

This project is open source and available under the MIT License.

## Acknowledgments

- GPT4All team for the local AI framework
- Mistral AI for the powerful language model
- Open-source community for continuous improvements
```
