# Heroku Custom Domain Tutorial

## Brief Introduction

Hello all. I wanted to make an in-depth guide on getting your deployed heroku application live on a custom domain. Unfortunately, the docs on heroku don't elaborate too well on their custom domain feature, so instead of going on a wild chicken-chase through 20+ websites to figure it out, I've developed this little guide to make it easy.

#### Please note a couple of Things before beginning
- You will need to have your heroku app of choice deployed and live (there are many tutorials for this else-where)
- Custom Domains aren't free! I will be including the steps to purchase a cheap google domain in this guide, so be willing to spend around $10

### Step 1

Head over to heroku, and click on your application. Go to your applications settings, and scroll down until you see a section about custom domains and SSL certificates.

<img width="500" alt="Screenshot 2023-07-25 at 3 51 03 pm" src="https://github.com/ThomasSzentirmay/Heroku-CustomDomain-Tut/assets/132217664/4de18d32-14c0-4e47-93b5-8a897846444a">

### Step 2

Click on 'add domain', and in the domain name input, type in what you wish your custom domain to be. By default, No SNI Endpoint will be set. You can leave that as it is, and click next.

<img width="500" alt="Screenshot 2023-07-25 at 3 54 16 pm" src="https://github.com/ThomasSzentirmay/Heroku-CustomDomain-Tut/assets/132217664/3b02a75a-a0af-4c71-b344-e797b50dcdf5">

### Step 3 

You should now see a DNS target. We will be using this over in the google domains site, so copy it to your clipboard.

<img width="500" alt="Screenshot 2023-07-25 at 3 58 37 pm" src="https://github.com/ThomasSzentirmay/Heroku-CustomDomain-Tut/assets/132217664/55837b4c-b8ec-414d-9f78-e2e8b9dfb50a">

### Step 4

Head to [this link](domains.google.com), and enter the domain you set in your heroku app. Purchase the domain. Note that if the domain you set in heroku is not available, choose one that is up for sale in google domains, and then go and edit it in your heroku settings. If the DNS target changes, make sure to copy it again!

### Step 5

After purchasing your domain, click on it. Then click on the 'DNS' tab on the left You will be taken to a settings page similar to below. If you can't see your domain, click on 'My Domains'. Note that your screen will look slightly different to mine below, as my custom domain is already set, but as long as you can see the 'Resource Records' section, than we can continue.

<img width="500" alt="Screenshot 2023-07-25 at 4 05 42 pm" src="https://github.com/ThomasSzentirmay/Heroku-CustomDomain-Tut/assets/132217664/bc9e6bcd-7004-4eef-9981-6b3e9839c3e7">

### Step 6

In the 'Host name' input, enter 'www'. In the 'Type' input, select 'CNAME'. In the 'TTL' input, select '10 minutes' (it will display as the number 600). Then, in the 'Data' input, paste your DNS target you copied from heroku. Click 'save'. See below for reference.

<img width="500" alt="Screenshot 2023-07-25 at 4 09 26 pm" src="https://github.com/ThomasSzentirmay/Heroku-CustomDomain-Tut/assets/132217664/f6b97b97-d943-48a1-af1a-7ae8bf4646e7">

### Step 7

Now that your google settings are saved, go back to your heroku settings, and scroll up to the SSL Certificates section above the DNS section. Click 'Automatic Certificate Management' (ACM), and click next.

<img width="500" alt="Screenshot 2023-07-25 at 4 15 51 pm" src="https://github.com/ThomasSzentirmay/Heroku-CustomDomain-Tut/assets/132217664/e7ea3d7c-5cfc-4159-bdbd-778b72b4cdb8">

### Step 8

Now you can scroll back down to your DNS section, and you will see a pending ACM status on your custom domain information. This should take a minute or two to confirm. Click 'Refresh ACM Status' to see when the status has turned to 'Ok' with a green tick!

<img width="500" alt="Screenshot 2023-07-25 at 4 20 19 pm" src="https://github.com/ThomasSzentirmay/Heroku-CustomDomain-Tut/assets/132217664/54ff8266-0ec9-4eef-9d40-4e0057d6be45">

You're website is now live on your custom domain! 

### Troubleshooting

There will always be the odd issue that could be caused for a multitude of reasons, but their are many ways to handle these, do don't worry.

- Search on the internet for people that have had the exact same problem as you > chances are they have found the fix for you
- See what ChatGPT has to say. Whilst it's not always the best tool to go to, it can definitely provide accurate insights on specfic issues
- Contact me. I would be happy to assist anyone facing specific issues when following this tutorial. I ran into quite a few myself, so reach out to me, and jopefully I can help you. Contact me [here](thomasszentirmay.com/contact)

Thanks for reading! 
