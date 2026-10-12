# Ollama commands

## Install ollama
```bash
curl -fsSL https://ollama.com/install.sh | sh
```

## Run model
```bash
ollama pull qwen3:8b
run ollama qwen3:8b
```

## Helpful commands
```bash
ollama --help
ollama list
nvidia-smi
```

## Modelfile in bash
sudo ollama create gemma4:e4b-8k -f Modelfile
sudo ollama run gemma4:e4b-8k

## Variable
OLLAMA_CONTEXT_LENGTH=64000 ollama serve

## Locations
Models: /usr/share/ollama/.ollama/models
Alternative package-managed location: /var/lib/ollama/.ollama/models
Executable: /usr/local/bin/ollama or /usr/bin/ollama
Systemd service: /etc/systemd/system/ollama.service or /usr/lib/systemd/system/ollama.service