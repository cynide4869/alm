# Anilist API Usage

A script to be able to save, delete or add new entries to default lists provided in anilist
- Planning
- Current
- Paused
- Re-Watching/Reading
- Dropped

# Dependencies

Run
```
pip install -r requirements.txt
```

Create a .env file in the same directory with the following parameters:
```
CLIENT_ID='ID_of_your_anilist_client'
CLIENT_SECRET='Client_secret_of_your_anilist_client'
NAME='Name_of_your_anilist_client'
```

To create an anilist client, go to [Anilist Developers Page](https://anilist.co/settings/developer)\
Create a new client and enter the redirect uri as [this](https://www.google.com/) or any other link of your choice\
Add the client id, secret and the name of the created client in the .env file

# Working

Uncomment either of the lines 249 - 251 to use the respective command

## Authentication

On running the script for the first time, it'll ask you to copy and paste a link to authenticate your account to the client, do so and copy the redirected link after authentication back in the terminal to add the access token to the .env file

## Required

- First run the file with storeUserMediaList uncommented for the list you want so that a json file for that category can be generated and the further functions can be used.
- The delete and save functions read from the json file generated by the store function.

To run the script, run
```
python main.py
```
