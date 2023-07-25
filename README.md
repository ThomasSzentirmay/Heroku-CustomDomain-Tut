# Heroku Custom Domain Tutorial

## Brief Introduction

Hello all. I wanted to make an in-depth guide on getting your deployed heroku application live on a custom domain. Unfortunately, the docs on heroku don't elaborate too well on their custom domain feature, so instead of going on a wild chicken-chase through 20+ websites to figure it out, I've developed this little guide to make it easy.

#### Please note a couple of Things before beginning
- You will need to have your heroku app of choice deployed and live (there are many tutorials for this else-where)
- Custom Domains aren't free! I will be including the steps to purchase a cheap google domain in this guide, so be willing to spend around $10

### Step 1

Head over to heroku, and click on your application. Go to your applications settings, and scroll down until you see a section about custom domains and SSL certificates.

<img width="750" alt="Screenshot 2023-07-25 at 3 51 03 pm" src="https://github.com/ThomasSzentirmay/Heroku-CustomDomain-Tut/assets/132217664/4de18d32-14c0-4e47-93b5-8a897846444a">

### Step 2

Click on 'add domain', and in the domain name input, type in what you wish you custom domain to be. By default, No SNI Endpoint will be set. You can leave that as it is, and click next.

<img width="750" alt="Screenshot 2023-07-25 at 3 54 16 pm" src="https://github.com/ThomasSzentirmay/Heroku-CustomDomain-Tut/assets/132217664/3b02a75a-a0af-4c71-b344-e797b50dcdf5">

### Step 3 

You should now see a DNS target. We will be using this over in the google domains site, so copy it to your clipboard.

<img width="750" alt="Screenshot 2023-07-25 at 3 58 37 pm" src="https://github.com/ThomasSzentirmay/Heroku-CustomDomain-Tut/assets/132217664/55837b4c-b8ec-414d-9f78-e2e8b9dfb50a">

