# Maid-chan bot
Telegram bot which helps me with channel uploads

## Setup
You need a `config.py` with those variables defined:
```python
channel = '<@main_channel_username | userid>'
nsfw_channel = '<@nsfw_channel_username | userid>'
master = '<master_userid>'
TOKEN = '<telegram_bot_token>'
db_auth = 'mongodb://<mongo_db_URI>'
db_name = '<database_name>'
```
You can use userid instead of any `@channel_name` for publishing to specified user instead of channel.
It is useful for testing.

## Starting bot
```
./app.py
```

## Usage
Maid forwards all messages except Master's to Master.
To reply from Maid to user, simply reply to forwarded message and Maid will resend your reply.

Maid tries to find high resolution for every recieved image. If found, she sends it to Master for confirmation.
