# Warframe Market Syndicate Automator

An experimental automation tool designed to dynamically manage and scale Syndicate offerings on `warframe.market`.

---

> [!CAUTION]
> **Disclaimer:** This project is a personal learning experience built with extensive use of AI assistance. It is completely independent and not affiliated with `warframe.market`. Automating platform interactions may violate their Terms of Service. **Use at your own risk.**

---

## 📌 Project Overview

This utility automates the process of converting in-game Syndicate standing into Platinum. Instead of manually listing individual mods and updating prices, the script acts as an automated manager that scales item quantities based on your inputted faction balance.

[ Standing Balance ] ──> [ Calculate Inventory ] ──> [ Live Market Ledger ]
(e.g., 100,000)          (100k / 25k = 4 units)         ( Cheaper by 1p )


---

## 📅 Project Status

This utility is currently fuctional but needs polishing. **there is no current timeline for a stable release.**

What Works For Now:
1) ~~login to your warframe.market account via jwt token. The token needs to be taken from your browser:~~
   - ~~after loggin in via browser f12 to open inspect view~~
   - ~~find the storage tab~~
   - ~~on the left seleect cookies~~
   - ~~warframe.market~~
   - ~~there should be only one entry "JWT"~~
   - ~~copy the value inside the settings.conf file in the root of the project (if the file doesn't exist, create it)~~
   - ~~now you are logged in~~ 
1) implemented setup in case settings.conf file is missing. Thanks to [JustMarkDev](https://github.com/JustMarkDev) for implementing this feature
2) use web interface to set standing for a syndicate, post all mods for syndicate with the click of a button
3) sell mods for syndicate with the click of other button

## TODO

1) ~~Web/Gtk interface for ease of use~~
2) rework GUI from ground up (streamlit sucks and not good to program with)
3)  A serious issue is the limit for listings that warframe.market sets for non-subscribers.
   To solve this issue, I need to post only the (5-10) most traded mods in the last 48 hours, possibly something the user can set for himself
   - The user may not want to sell as fast as possible, but to gain as much platinum per standing as possible. Should implement a function
   that allows the user to choose how much weight it gives to the most traded mods, and how much to the ones that sell for more. 
4) ~~I began to create the web interface, but the logic is wonky, and there are 2 main issues i need to address:~~
   - ~~error in the logic that recomputes the available standing after you sell mods~~
   - ~~the slider doesn't visually update after selling~~
5) more functionalities, like mass post relics, post all relics sold by varzia and whatever comes to mind next

