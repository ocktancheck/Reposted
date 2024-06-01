from telethon.sync import TelegramClient

api_id = 13303996
api_hash = '75800319a9c28f9d63df50bfbfc20d95'

source_channel_id = -1002230002038
target_channel_id = -1002208888016

client = TelegramClient('session_name', api_id, api_hash)

async def main():
    await client.start()
    async for message in client.iter_messages(source_channel_id):
        await client.forward_messages(target_channel_id, message)

with client:
    client.loop.run_until_complete(main())
