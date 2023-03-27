## Web (MEAN) Stack implementation in AWS.

#This project demonstrates how to build a MEAN Stack on AWS. MERN stack consists of MongoDB, ExpressJS, ReactJS and Node.js. Our goal here is to implement a simple Book Register web form using MEAN stack.

![MEAN_stack](./images/mean.jpeg)

## .............................. Step 1: Launch an Ubuntu Server on AWS ..............................

For this project, we will need a virtual server with Ubuntu Server OS.

Sign in as either the root/IAM user (good practice is to create an IAM user and not use the root user to create resources on AWS).
Create and launch an Ubuntu EC2 instance (check videos below on how to set up your AWS account and launch your first EC2 instance).

- [AWS account setup and Provisioning an Ubuntu Server] (https://www.youtube.com/watch?v=xxKuB9kJoYM&list=PLtPuNR8I4TvkwU7Zu0l0G_uwtSUXLckvh&index=6)
- [Connecting to your EC2 Instance] (https://www.youtube.com/watch?v=TxT6PNJts-s&list=PLtPuNR8I4TvkwU7Zu0l0G_uwtSUXLckvh&index=7)

## .............................. Step 2: Install NodeJs ..............................

Node.js is a JavaScript runtime built on Chrome’s V8 JavaScript engine. We are using Node.js in this tutorial to set up the Express routes and AngularJS controllers.

Update and Upgrade your Ubuntu instance:

**`sudo apt update`**
**`sudo apt upgrade`**

Next, we add certificates:

**`sudo apt -y install curl dirmngr apt-transport-https lsb-release ca-certificates`**

**`curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -`**

Install NodeJS

**`sudo apt install -y nodejs`**

![nodeJS](./images/nodejs.png)

## .............................. Step 3: Install MongoDB ..............................

MongoDB stores data in flexible, JSON-like documents. Fields in a database can vary from document to document and data structure can be changed over time. For our simple Book Register web application, we will be adding book records to MongoDB that contain book name, isbn number, author and number of pages. 