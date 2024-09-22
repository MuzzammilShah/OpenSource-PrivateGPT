### **SETUP DOCUMENTATION**

--------------------------
--------------------------

#### **METHOD 2 - Local Setup**

**Versions Pre-requisites:**
- Python version: 3.11
- Poetry version: >=1.7

##### **SET 1**
--------------------------

- In WSL, The default ubuntu version maybe 3.10. Therefore we need to upgrade it.

**Follow these series of commands in order**

```
sudo add-apt-repository ppa:deadsnakes/ppa
```

```
sudo apt install python3.11
```
*(Note: Here, you may encounter an issue where python3.11 wont install (If not, you can ignore this note). It maybe due to some broken packages. **To fix this, use the command:** sudo dpkg --configure -a)*

```
sudo apt install python3.11-venv
```

- Now, only the installations have been done. We need to update it to a different version.

```
sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.10 110
```

```
sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.10 100
```

```
sudo update-alternatives --config python3
```

*After runnning the above command, select the number/option of which python version you want to run.*

```
python3 -m pip install pip
```

**Installing Poetry**

```
pip install poetry
```

Make sure to check its version is >=1.7.0

```
poetry --version
```


##### **SET 2**
--------------------------

**Reference: [PrivateGPT Documentation](https://docs.privategpt.dev/installation/getting-started/installation#local-ollama-powered-setup---recommended)**


**Pre-requisites:**

- Clone the repository

```
git clone https://github.com/zylon-ai/private-gpt.git
```

```
cd <repo-directory>
```

- Create virtual environment

```
python3 -m venv venv
```

- Activate virtual environment

```
source venv\bin\activate
```

**Documentation recommended steps:**

- Check if ollama is running

```
ollama serve
```

```
poetry install --extras "ui llms-ollama embeddings-ollama vector-stores-qdrant"
```

```
PGPT_PROFILES=ollama make run
```

*If the run was successfull you should see the http://localhost:8001*
*Use Ctrl+C to Quit*

--------------------------
--------------------------