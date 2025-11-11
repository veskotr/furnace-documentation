We are using the Google Firebase Server Hosting.

It's [parameters and cost](https://firebase.google.com/pricing) align well with our expectations for traffic and storage.

In the future I will look at and compare more server hosting services, but for now, this is good enough
## Installation

In this section I will go through the process of setting up hosting on Firebase. I will go in-depth of all steps as this aims to be a comprehensive guide.

This process is true as of 10.11.2025.

### Step 1: Google Account

First step is to have a google account.

Depending on the client need we can create a [normal account](https://accounts.google.com/) or a business one with [google workspace](https://workspace.google.com/) which is a paid service. The main benefits of having a business account are listed [here](https://workspace.google.com/pricing) based on your payment plan.

In most cases we can work with a "personal" account which is free of charge.

***There is a problem to consider:*** 
1. *Are we going to be the owners of the accounts, or are our clients going to be?* 
2. *If we hold the accounts, do we take the responsibility for paying and upkeep of the server?*
3. *Are we going to offer a subscription or payment for this service?* 
4. *Are we going to leave our clients do the work potentially appearing as a "worse" service?*
5. *Same goes for the server, in most cases it will be free upkeep but what if the pricing and free tiers change?*

### Step 2: Firebase Account

This is a simple step. Just go to the [Firebase website](https://firebase.google.com/) and log in using your google account.

### Step 3: Download and install npm (Node.js Package Manager)

First go to the [official website for Node.js](https://nodejs.org/en/download) and download the prebuild Node.js for your system and architecture.

![[Pasted image 20251110171945.png]]

When the download finishes, start the installer and follow instructions.

After you are done with installing the product - open your system command line interface:

On Mac: use the search function in your bar and type terminal.app and hit enter.

Windows - press the windows key and "r" key. This opens a little window: ![[Pasted image 20251110172256.png]]

In it type "cmd" and hit enter. A new window will open:![[Pasted image 20251110172645.png]]

 In this window, after the last symbol, type: 
```
  node -v
```

If the installation ran correctly and without errors - you will have a similar message (version may vary) show below the text:
![[Pasted image 20251110173456.png]]

If you see this message, type this next:
```
nmp -v
```

If this runs and you get a version text
![[Pasted image 20251110173729.png]]
like the one above (they don't need to be the same version), the you are good to proceed to step 4

### Step 4:  Set up the project in Firebase

Enter the [Firebase website](https://firebase.google.com/) and find a button or a link to the "console":
![[Pasted image 20251110173952.png]]

When you enter the page, click on create a new Firebase project and follow the wizard.
![[Pasted image 20251110174227.png]]

After you are done, open the command line interface again and type:
```
npm install -g firebase-tools
```


After the installation is done type:
```
firebase login
```

The some prompts will follow, type "Y" or "n" if you agree or disagree. After you are done, a browser window will open and prompt you to long in with a google account. After a successful login, the console should say "Success! logged in as your account." and 