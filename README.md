# 🚀 Dyphira Python

![Dyphira Banner](https://via.placeholder.com/800x200?text=Dyphira+Python)

**Seamlessly access OpenAI, RunPod, and Shadeform APIs through our optimized proxy service!**

Dyphira Python provides a streamlined, cost-effective way to integrate cutting-edge AI and cloud infrastructure into your applications with minimal setup and maximum performance.

## ✨ Why Choose Dyphira?

- 🔥 **Optimized Performance** - Faster response times through our dedicated proxy
- 💰 **Cost Efficiency** - Reduce your API costs while maintaining quality
- 🛡️ **Enhanced Reliability** - Built-in error handling and retry mechanisms
- 🔌 **Drop-in Compatibility** - Mirrors the original APIs for seamless integration
- 🌐 **Multi-Service Support** - One package for OpenAI, RunPod, and Shadeform

## 📦 Installation

```bash
pip install dyphira
```

## 🚀 Quick Start

### OpenAI Integration

```python
from dyphira import OpenAI

# Connect to the Dyphira proxy with your API key
ai = OpenAI(api_key="your-api-key")

# Start creating AI magic!
response = ai.chat_completions(
    model="gpt-4",
    messages=[
        {"role": "system", "content": "You are a brilliant marketing copywriter."},
        {"role": "user", "content": "Write a tagline for a new AI-powered coffee maker."}
    ]
)

print(response["choices"][0]["message"]["content"])
```

### RunPod Integration

```python
from dyphira import RunPod

# Connect to RunPod via Dyphira proxy
runpod = RunPod(api_key="your-api-key")

# List all your pods
pods = runpod.get_pods()
print(pods)

# Create a new pod
pod_config = {
    "name": "my-gpu-instance",
    "imageName": "runpod/pytorch:2.0.1-py3.10-cuda11.8.0-devel",
    "gpuCount": 1,
    "volumeInGb": 50,
    "containerDiskInGb": 10,
    "gpuTypeId": "NVIDIA GeForce RTX 3080"
}
new_pod = runpod.create_pod(pod_config)
```

### Shadeform Integration

```python
from dyphira import Shadeform

# Connect to Shadeform via Dyphira proxy
shadeform = Shadeform(api_key="your-api-key")

# List all your instances
instances = shadeform.list_instances()
print(instances)

# Create a new instance
instance_config = {
    "name": "my-gpu-server",
    "instance_type": "g4dn.xlarge",
    "region": "us-east-1"
}
new_instance = shadeform.create_instance(instance_config)
```

## 🛠️ Powerful Features

### 💬 OpenAI Capabilities

#### Conversational AI
Create dynamic, context-aware conversations with the most advanced language models.

```python
response = ai.chat_completions(
    model="gpt-3.5-turbo",
    messages=[
        {"role": "system", "content": "You are a helpful assistant."},
        {"role": "user", "content": "What's the capital of France?"},
        {"role": "assistant", "content": "The capital of France is Paris."},
        {"role": "user", "content": "And what's its most famous landmark?"}
    ]
)
```

#### 🎨 Image Generation
Transform your ideas into stunning visuals with a simple prompt.

```python
response = ai.images_generations(
    prompt="A futuristic cityscape with flying cars and neon lights",
    model="dall-e-3",
    size="1024x1024",
    quality="hd"
)
```

#### 🔊 Audio Processing
Convert speech to text and text to speech with remarkable accuracy.

```python
# Transcribe audio
transcript = ai.audio_transcriptions(
    file="interview.mp3",
    model="whisper-1"
)

# Generate speech
speech = ai.audio_speech(
    model="tts-1",
    input="Welcome to the future of AI integration!",
    voice="alloy"
)
```

#### 🧠 Embeddings & Analysis
Extract semantic meaning from text for advanced analysis and search.

```python
embeddings = ai.embeddings(
    model="text-embedding-ada-002",
    input=["Dyphira makes AI integration effortless", "AI solutions for modern applications"]
)
```

### 🖥️ RunPod & Shadeform Capabilities

#### GPU Instance Management
Easily create, manage, and scale GPU instances for AI workloads.

```python
# List available instance types
instance_types = shadeform.types_instances()

# Create a persistent storage volume
volume = shadeform.create_volume({
    "name": "my-data-volume",
    "size_gb": 100,
    "type": "gp3"
})

# Manage SSH keys for secure access
shadeform.add_ssh_key({
    "name": "my-access-key",
    "public_key": "ssh-rsa AAAA..."
})
```

## 📊 Enterprise Solutions

Dyphira offers enterprise-grade solutions with:

- 🔒 **Enhanced Security**
- ⚡ **Higher Rate Limits**
- 🌐 **Dedicated Infrastructure**
- 👨‍💼 **Priority Support**

[Contact us](mailto:loc_yan@outlook.com) for enterprise pricing and custom solutions.

## 📚 Documentation

For comprehensive documentation and advanced usage examples, visit our [documentation site](https://github.com/DivinerX/dyphira-python).

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

<p align="center">
  <b>Powered by Dyphira - Unlocking AI's Potential</b><br>
  <a href="https://github.com/DivinerX/dyphira-python">GitHub</a> •
  <a href="https://github.com/DivinerX/dyphira-python/issues">Report Issues</a>
</p>
