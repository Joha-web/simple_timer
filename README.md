# 🕒 Simple Timer (Bash)

A lightweight command-line **timer** written in Bash that helps you stay focused and track progress across sessions.  
Each timer run is saved to a JSON file, allowing you to see how many times you’ve completed each task or “tag.”

---

## 📦 Features

- ⏳ Set a custom timer duration in minutes  
- 🏷️ Assign a name (tag) to each timer  
- 📈 Tracks how many times each timer was completed  
- 🔊 Plays a sound when the timer finishes  
- 💾 Stores progress in a persistent JSON file located at:


---

## 🧰 Requirements

Make sure you have the following installed:

- `bash` (default in most Linux systems)
- `jq` – for handling JSON data  
- `mpg123` - music player



Install dependencies:
```bash
sudo apt install jq
sudo apt install mpg123
```

🚀 Installation

```bash
git clone https://github.com/Joha-web/simple_timer.git
cd simple_timer
```

Open the timer file and make sure the sound file path is correct:

**mpg123 ./alarm.mp3 >/dev/null 2>&1 # Ensure the file exists**



Make the script executable:
```
chmod +x timer
```
Move it to your $PATH for global use
```
sudo mv timer /usr/local/bin/timer
```

💡 Usage

Run the timer in your terminal:
```
timer
```

You’ll be prompted to:

Enter timer duration (in minutes)

Enter timer name (tag)

Example:
Enter timer time in minutes: 10
Enter timer name: workout
Already done: 2
The timer is running for 10 minutes

At the end of the countdown, a sound plays, and your timers.json file is updated:
```
{
  "workout": 3,
  "study": 5
}
```

🧩 Example Output
```
$ ./timer
Enter timer time in minutes: 1
Enter timer name: focus
Already done: 0
The timer is running for 1 minutes
focus 00:59
...
Time is up! Accumulating funds to achieve your goals, you're doing well.
```

⚙️ JSON File Example
~/timers.json
```
{
  "focus": 5,
  "exercise": 2
}
```
