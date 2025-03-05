# Walme Auto Bot

An automated bot for completing Walme airdrop tasks with comprehensive proxy support (HTTP, SOCKS4, SOCKS5).

## Register

- https://waitlist.walme.io?inv=AWILZZ

## Features

- 🚀 Automatically completes all available Walme waitlist tasks
- ✅ Daily check-in for the 7-Day Challenge XP Boost
- 🔄 Automatic rescheduling for continuous operation 
- 🌐 Complete proxy support (HTTP, SOCKS4, SOCKS5)
- 📊 Detailed logging with colorful console output
- 👥 Multi-account support through tokens.txt
- 🔄 Tracks completed tasks to avoid duplication

## Requirements

- Node.js (v16 or higher)
- npm (Node Package Manager)
  
# How to Get Your Access Token

1. Open your browser and login to the Walme dashboard.
2. Press `F12` to open the **Inspect Elements** panel.
3. Go to the **Console** tab and paste the following code:

   ```javascript
   localStorage.getItem('accessToken')
   ```

4. You will receive your user ID, which looks like this: `"eyjxxxx........"`
5. If you can't paste, type allow pasting and press Enter, then paste the line above.

## Installation

1. Clone the repository:
```bash
git clone https://github.com/Not-D4rkCipherX/Walme.git
cd Walme
```

2. Install dependencies:
```bash
npm install
```

## Configuration

1. Set Up Accounts
    ```bash
   nano data.txt
   ```
   - Now Add one NodeGo access token per line
   - Example:
     ```
     token1
     token2
     token3
     ```

3. (Optional) Proxy
 ```bash
nano proxies.txt
```
   - Add one proxy per line
   - Supports both HTTP and SOCKS proxies
   - Example:
     ```
     http://ip1:port1
     socks5://ip2:port2
     socks4://ip3:port3
     ```
## Usage

Run the bot:
```bash
node index.js
```

The bot will:
1. Load your tokens from tokens.txt
2. Load proxies from proxies.txt (if available)
3. Process each account, completing all available tasks
4. Check in for the 7-Day Challenge
5. Repeat the process every 24 hours

## Proxy Support

The bot supports various proxy formats:

- HTTP proxies: `http://user:pass@host:port` or `host:port`
- SOCKS4 proxies: `socks4://user:pass@host:port`
- SOCKS5 proxies: `socks5://user:pass@host:port`

The script will rotate through available proxies, assigning them to accounts in a round-robin fashion for optimal distribution.

## Troubleshooting

If you encounter issues:

- Make sure your tokens are valid and properly formatted in tokens.txt
- Check that your proxies are working and properly formatted in proxies.txt
- Verify that you have installed all required dependencies
- Check the console for detailed error messages
  
## Disclaimer

This tool is for educational purposes only. Use at your own risk. The developers are not responsible for any account actions resulting from the use of this bot.
