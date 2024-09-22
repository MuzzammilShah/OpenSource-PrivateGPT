### **INTRODUCTION**
-------------------------

- AI Model is essentially an Artificial Intelligence that is pre-trained on our data.

#### **WSL (Windows Subsystem for Linux)**

*Remember to check path to the directory, need to have Admin priviledge*

```
wsl --install
```

```
ollama run <model-name>
```

(On WSL, if NVIDIA doesn't show up, we'll have to get those drivers installed)

#### **RAG (Retrieval Augmented Generation)**

- A vector Database

- So, we're not retraining the LLM. We're just saying: Hey, before you answer, just check in there (DB) real quick and see if you have the updated information.
![Explaination Diagram]()

--------------------------
--------------------------

#### **WORKING WITH WSL**

For entering into ubuntu terminal from windows:

```
wsl -d ubuntu
```

```
exit
```

To check all of my linux files inside windows explorer:

```
explorer.exe .
```

To check GPU version through Ubuntu terminal:

```
nvidia-smi
```

--------------------------
--------------------------