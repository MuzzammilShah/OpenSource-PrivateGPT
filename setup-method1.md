### **SETUP DOCUMENTATION**

--------------------------
--------------------------

#### **METHOD 1 - WSL, Docker -> WebUI**

- Admin cmd

```
wsl install
```

- Enter WSL 

```
wsl -d ubuntu
```

- CLI from [Ollama website](https://ollama.com/download/linux) for installation.

- Check if it has been successfully installed

```
ollama
```

- Run the model:

```
ollama run <model-name>
```

- Install necessary VS Code extensions: wsl, docker

- Install Docker Desktop

- Get docker run command from the [WebUI GitHub Repo](https://github.com/open-webui/open-webui?tab=readme-ov-file#quick-start-with-docker-)

```
docker run -d -p 3000:8080 --gpus all --add-host=host.docker.internal:host-gateway -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:cuda
```
*Have added the one I used, run only if NVIDIA GPU is activated.*

--------------------------
--------------------------