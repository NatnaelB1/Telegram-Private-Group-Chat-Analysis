# 📊 Telegram Chat Analysis  

Analyze Telegram group chats with Python and Jupyter Notebooks to uncover trends, message patterns, and user behaviors.  

## Inspiration
This fun project was inspired by Spotify Wrapped. I started it when I realized that the Telegram group chat I share with five close friends was six years old. 
This made me wonder what a "Wrapped" for all those years of data would look like—what trends we could uncover and how our conversations had evolved over those years.

From the initial combined Wrapped code I wrote, I modified and modularized the code so that I can run it every year without having to rewrite it. Now, it’s a reusable tool for analyzing and visualizing group chat history for anyone!

## 🚀 Features  
✔ **Message Statistics** – Count messages per user: daily/monthly/yearly trends. 

✔ **Activity Trend** – Active and inactive times of a day/week/month/year.

✔ **Visualizations** – Generate bar charts, stacked plots, and other insightful graphs.

✔ **Mentions Tracking** – Find how often specific words or users are mentioned.  

✔ **Conversation Patterns** – Identify who starts conversations and how long they last.  

✔ **Reaction & Emoji Analysis** – Track emoji usage and who reacts the most.  

## 📂 Data Processed  
- **Messages** – Sent messages, timestamps, and users.  
- **Reactions** – Who reacted and which emojis were used.  
- **Mentions** – Count how often a word/user appears.  
- **Conversations** – Length and time gaps between messages.


## 🛠️ Setup & Installation  

### 1️⃣ Clone the repository:  
```sh
git clone https://github.com/NatnaelB1/Telegram-Private-Group-Chat-Analysis.git
cd Telegram-Private-Group-Chat-Analysis-main
```

### 2️⃣ Set up a virtual environment (optional but recommended):
```sh
python -m venv venv

source venv/bin/activate # For macOS/Linux:
venv\Scripts\activate # For Windows
```

### 3️⃣ Install dependencies:
```sh
pip install -r requirements.txt
```

### 4️⃣ Launch Jupyter Notebook:
```sh
jupyter notebook
```

### 5️⃣ Load your Telegram JSON export into the notebook and run the analysis.
📦 Dependencies
* Python >=3.10.9

📜 How to Get Telegram Data

1️⃣ Open Telegram Desktop

2️⃣ Go to settings: Click the menu (three horizontal lines) in the top left, then select Settings > Advanced.

3️⃣ Choose Export Telegram Data: Scroll down to Export Telegram data

4️⃣ Select what to back up: select Private groups **only** in chat export settings

5️⃣ Start export: Scroll down, select Machine-readable JSON format, and click Export (Export might take a few mins).



### 🛠️ **Final Setups**

1️⃣ After the data download is complete, place the downloaded file in the project directory. 

2️⃣  In the third code block, update file_name with the name of your data download
```python
# TODO: Ensure your Telegram data JSON file is placed in the current directory.
# TODO: Change 'test.json' to the actual downloaded chat data name.

file_name = "test.json"  # Update this string with the name of your data download

# Check if the file exists before attempting to open it
if os.path.exists(file_name):
    with open(file_name, "r", encoding="utf-8") as file:
        data = json.load(file)
    print(f"✅ Successfully loaded '{file_name}'")
else:
    print(f"❌ Error: File '{file_name}' not found. Please place it in the current directory.")
```

### 💡 Future Improvements
✅ Advanced sentiment analysis on messages.

✅ More interactive dashboards using Plotly or Streamlit.

### 🤝 Contributions
Feel free to fork, create issues, or submit pull requests!

