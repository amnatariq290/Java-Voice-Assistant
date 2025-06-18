# 🗣️ Java Voice Command Recognition with Sphinx4

This project is a simple Java-based voice command recognition application using the **CMU Sphinx4** library. It listens to your microphone input and detects predefined voice commands using a grammar-based approach (JSGF).

---

## 🚀 Features

- 🎙️ Real-time voice command recognition  
- 📖 Grammar-based recognition using `.jsgf`  
- 💻 Works offline, no internet needed  
- 🔧 Easily extensible with new commands

---

## 🧰 Requirements

- Java JDK 8 or higher  
- Eclipse / IntelliJ / NetBeans or any Java IDE  
- Sphinx4 JAR files  
- Microphone

---

## 📁 Project Structure

SpeechRecognitionProject/ ├── src/ │ └── SpeechRecognitionExample.java ├── resources/ │ ├── grammar/ │ │ └── commands.jsgf │ └── dictionary.dict ├── lib/ │ └── (Sphinx4 JAR files) ├── README.md


---

## 📦 JAR Files Needed

Place these JAR files inside the `lib/` folder (download from the [Sphinx4 GitHub repo](https://github.com/cmusphinx/sphinx4)):

- `sphinx4-core.jar`
- `sphinx4-data.jar`
- `sphinx4-common.jar`
- `sphinx4-util.jar`
- `sphinx4-signal.jar`
- `jsapi.jar`

---

## 🔧 Setup Instructions

1. **Clone or Download the Project**

```bash
git clone https://github.com/amnatariq290/speech-recognition-java.git
cd speech-recognition-java

Open in your IDE
Import the project and add all JARs in the lib/ folder to your project's build path.

Set Resource Paths in Code

In SpeechRecognitionExample.java, make sure to configure these paths:
configuration.setAcousticModelPath("file:resources/acoustic-model");
configuration.setDictionaryPath("file:resources/dictionary.dict");
configuration.setGrammarPath("file:resources/grammar");
configuration.setGrammarName("commands");
configuration.setUseGrammar(true);

4.Run the Program
Click Run in your IDE

Speak into the microphone using one of the defined commands
It will print the recognized command.

Command File:commands.jsgf
#JSGF V1.0;
grammar commands;
public <command> = and | the | none | boo | mm | hm | and with | no | how | who | what | it happened ;
You can modify this file to add or remove commands easily.

💡 Tips
Speak clearly and close to the mic

You can add more words in commands.jsgf and handle them in the Java code

Check your dictionary file (dictionary.dict) has phonemes for every word in grammar

👩‍💻 Author
Amna Tariq

