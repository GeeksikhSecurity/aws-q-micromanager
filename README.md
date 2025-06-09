# AWS Q MicroManager

A collection of specialized AI modes for AWS Q Developer to optimize AI assistance through intelligent task orchestration.

Inspired by [RooCodeMicroManager](https://github.com/adamwlarson/RooCodeMicroManager) by Adam Larson ([@adamwlarson](https://github.com/adamwlarson)).

## Motivation

In the evolving landscape of AI development, where free access to powerful models is becoming increasingly limited, cost optimization becomes crucial. AWS Q MicroManager addresses this challenge through intelligent task orchestration:

- **Cost-Efficient Workflow**: Instead of using the most expensive model for every task, MicroManager intelligently delegates work to appropriately sized models based on task complexity
- **Model Optimization**: Each specialized mode is configured with the most cost-effective model that can handle its specific responsibilities, with AWS Q Developer as a primary option
- **Resource Allocation**: Simple tasks are handled by smaller, more affordable models, while complex tasks are reserved for more capable models
- **Future-Proofing**: As AI services move towards paid models, this approach ensures sustainable development practices by optimizing resource usage

## Getting Started

1. Copy the prompt files from the `prompts` directory to your AWS Q saved prompts directory:
   ```
   cp prompts/* ~/.aws/amazonq/prompts/
   ```

2. Start with MicroManager mode by typing `@prompt MicroManager` in AWS Q chat

3. MicroManager will analyze your task and recommend appropriate specialized modes

4. Switch to recommended modes using `@prompt [ModeName]` (e.g., `@prompt Senior`)

## Available Modes

- **MicroManager**: The orchestrator mode that coordinates complex tasks
- **Intern**: For simple, well-defined implementation tasks
- **Junior**: For slightly complex implementation tasks
- **MidLevel**: For broader implementation tasks
- **Senior**: For complex, multi-file implementations
- **Designer**: For UI/UX design and styling
- **Researcher**: For codebase research and analysis
- **Architect**: For high-level planning and architectural decisions
- **CodeShortRules**: Optimized for models with limited context windows

## Workflow Example

1. Start in MicroManager mode with your task
2. MicroManager analyzes the task and creates a plan
3. Tasks are delegated to appropriate modes:
   - Planning → Architect
   - Simple implementation → Intern
   - Complex implementation → Senior
   - UI/UX → Designer
   - Research → Researcher
4. Results are synthesized and presented back to you

## Model Recommendations

Each mode is optimized based on the capabilities of various AI models:

| Mode | Recommended Model |
|------|------------------|
| MicroManager | AWS Q Developer or Gemini 2.5 Pro Preview |
| Intern | AWS Q Developer or Llama 3.1 Nemotron 253B |
| Junior | AWS Q Developer or GPT 4.1 mini |
| MidLevel | AWS Q Developer or GPT 4.1 |
| Senior | AWS Q Developer or Gemini 2.5 Pro Preview |
| Designer | AWS Q Developer or Claude 3.7 |
| Researcher | AWS Q Developer or Gemini 2.0 Flash |
| Architect | AWS Q Developer or Claude 3.7 |
| CodeShortRules | AWS Q Developer or any local model |