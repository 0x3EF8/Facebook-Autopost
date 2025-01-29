# facebook autopost

This script automates posting to your Facebook timeline using Selenium and the Gemini API.

## Installation

1. Ensure you have Python 3.7 or higher installed on your system.

2. Clone this repository or download the script files.

3. Install the required packages using pip:

```
pip install -r requirements.txt
```

## Configuration

1. Create a configuration file named `config.ini` in the root directory of the project with the following content:

```ini
[Facebook]
email = your_facebook_email
password = your_facebook_password

[Gemini]
api_key = your_gemini_api_key

[PostGeneration]  
prompt = your_post_prompt

[Automation]
post_interval = interval_in_seconds
profile_name = your_profile_name (optional, default is "default")
```

## Usage

```
python3 main.py
```

## How It Works

1. **Initialization**: The script initializes the `FacebookAutoPost` class with your Facebook credentials, Gemini API key, post prompt, post interval, and profile name.

2. **Profile Setup**: It sets up a browser profile path to store browser data.

3. **Driver Setup**: It configures the Selenium WebDriver with Chrome options and sets up the driver.

4. **Gemini API Setup**: It initializes the Gemini API with the provided API key.

5. **Previous Posts**: It loads previously posted content to avoid duplicate posts.

6. **Posting**: The script logs into Facebook, generates a post using the Gemini API, and posts it to your timeline at the specified interval.

## Notes

- Keep your configuration file (`config.ini`) secure as it contains sensitive information.
- Ensure ChromeDriver is installed and its path is correctly set in your environment variables.
- The script uses a headless browser by default for automation.
- Adjust the `post_interval` in the configuration file to control how frequently posts are made.
- The `profile_name` can be used to create separate browser profiles for different Facebook accounts or settings.