# DBZ Dokkan Battle web scraper 9000

This repo scrapes the Dokkan Battle [wiki](https://dbz-dokkanbattle.fandom.com/wiki/Dragon_Ball_Z_Dokkan_Battle_Wiki) to create a csv/excel file for all story events and all UR/LR characters in the game.

- [Introduction](#introduction)
- [What can I do with this data?](#what-can-i-do-with-this-data)
- [How to use this tool](#how-to-use-this-tool)

## Introduction

I wrote this script after coming back from a 2 years brake from the game. I was overwhelmed with all the content that I had to play and I did't know on what to focus first. Generally speaking newer events and newer characters are often better and/or more relevant that older events and characters. The DBZ Dokkan Battle wiki is great but it does **not show** you a **list** of **all story events or characters sorted by release date**. Therefore I created this script to scrap through the DBZ DB wiki and get the release dates + some other information mentioned below and create a csv/excel export.
The script creates 2 different csv/excel files:

1. dbz_db_characters_YYYY_MM_DD.csv/xlsx: This file contains information about all Story events in DBZ Dokkan Battle
2. dbz_db_characters_YYYY_MM_DD.csv/xlsx: This file contains information about all UR/LR characters in the game

The story events file includes the following information:

- Event name
- Global release
- Japan release
- Url

The characters file includes the following information:

- Name
- Rarity
- Class
- Type
- Global release
- Japan release
- Global EZA release
- Japan EZA release
- Global EZA
- Japan EZA
- HP 55%
- ATK 55%
- DEF 55%
- HP 100%
- ATK 100%
- DEF 100%
- HP 55% EZA
- ATK 55% EZA
- DEF 55% EZA
- HP 100% EZA
- ATK 100% EZA
- DEF 100% EZA
- Categories
- Card ID
- Url

## What can I do with this data?

As with any Excel table you can sort and filter the data however you like.

For example: Showing all Super class characters that are part of "Kamehameha" category, released after 2023-01-01 and orderd by release date descending.

![ExcelTable](https://i.imgur.com/E5AN3Q4.png)

Here is a sreenshot of the story events sorted by release date descending:
![CSVTable](https://i.imgur.com/psBtyFQ.png)

## How to use this tool

If you want to get the latest data you have to run the script yourself.

### For normal users

If you have no idea of coding whatsoever just follow these steps:

1. Go to [Google colab](https://colab.research.google.com) and login in with you google account (it's free)
2. Click on "New notebook" in case you are asked
3. Copy everything in the file [dbz-db-scraper-colab-version.py](dbz-db-scraper-colab-version.py)
4. Paste the entire code in colab and click the run icon
5. Wait until it is finished (it will take around 10 minutes)
6. Click on the file icon on the very left
7. There you will find your new csv/excel file. You can also download it to your local machine
8. Profit

### For developers

Make sure have python 3.6 or newer installed.

1. Open command line and navigate to a directory of your choice.
2. Clone this repository to your machine via the following command:

```shell
git clone https://github.com/Daniel-Fauland/dokkan-battle.git
```

3. Navigate to the cloned repository:

```shell
cd dokkan-battle
```

4. Install requirements

```shell
pip install requirements.txt
```

5. Run script

```shell
python dbz-db-scraper.py
```

Note:
I could have also created a python package for extracting information from dbz dokkan wiki pages but I was to lazy tbh.
However in case anyone wants to that feel free to use my code. Certain functions can probably be used with very little changes necessary to extract certain information.
BTW: The only difference between the normal py and colab version is that there are slightly different prints in the colab version as colab notebooks do not support prints with end='\r'
