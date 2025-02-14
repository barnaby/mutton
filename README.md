# 🐑 Mutton

**Mutton** is like *Ollama for the cloud:* a simple command-line tool that lets you deploy and manage open-source large language models (LLMs) across your own cloud infrastructure—without the hassle. Currently supporting **AWS**, **Azure**, and **Runpod**, with more on the way.

## Why Mutton?

- 💰 **No expensive hardware needed**  
  Run the latest open-source models at full speed using cloud GPU instances.  

- 🚀 **Deploy in minutes**  
  Spend more time building and less time wrestling with DevOps.  

- 🛡️ **Total control**  
  Keep your data where you want it and decide who can access it.  

- 🏗️ **Flexible & portable**  
  Avoid vendor lock-in and switch cloud providers easily.  

- ⚙️ **Hassle-free management**  
  A simple CLI for deploying, starting, stopping, and tearing down models.  

- 🔧 **Terraform under the hood**  
  Reliable infrastructure-as-code with minimal setup.

## Who’s it for?

- 🧑‍💻 **Tinkerers & Indie Developers**  
  An easy way to experiment with and deploy open-source LLMs.

- 🏢 **Companies**  
  Host models on existing cloud infrastructure or maintain data privacy and compliance.

## How it Works

### Installation (macOS)

```bash
$ brew install mutton
```

### Deploy a model

```bash
# Deploy a large language model
$ mutton deploy
Which cloud provider [AWS, Azure, Runpod]: AWS
oAuth with Amazon...
Select Model: Deepseek-R1
# ...
```

### Chat
```bash
$ mutton chat 846590
Chatting with Deepseek-R1
> write a short story
once up a time in ...
```

### Manage Your Deployments

```bash 
$ mutton ls
Model Id    Model Name     Cloud    GPU     Uptime
846590      Deepseek-R1    AWS      A100    30m

# Stop a deployment
mutton stop 846590

# Start it again
mutton start 846590

# Completely remove a model and its data
mutton kill 846590
```
