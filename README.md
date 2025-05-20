Decentralized-Voting-System-Using-Ethereum-Blockchain

The Decentralized Voting System using Ethereum Blockchain is a secure and transparent solution for conducting elections. Leveraging Ethereum's blockchain technology, this system ensures tamper-proof voting records, enabling users to cast their votes remotely while maintaining anonymity and preventing fraud. Explore this innovative project for trustworthy and decentralized voting processes.



Screenshots
![](https://github.com/AskhatSBK/final_proj_blockchain/blob/adf20bbba2559977787fc82ece3d51856f84cb6f/public/35593211-b158-4ed2-9cb7-1c50fcc803e6.png)
![](https://github.com/AskhatSBK/final_proj_blockchain/blob/adf20bbba2559977787fc82ece3d51856f84cb6f/public/44d41fc2-7050-4a38-8692-65f213e0e65f.png)
![](https://github.com/AskhatSBK/final_proj_blockchain/blob/adf20bbba2559977787fc82ece3d51856f84cb6f/public/7e2348a5-8b34-4a99-8c8e-08cd7af4fff6.png)
Installation

Open a terminal.

Clone the repository by using the command

 git clone https://github.com/Krish-Depani/Decentralized-Voting-System-Using-Ethereum-Blockchain.git

Download and install Ganache.

Create a workspace named developement, in the truffle projects section add truffle-config.js by clicking ADD PROJECT button.

Download Metamask extension for the browser.

Now create wallet (if you don't have one), then import accounts from ganache.

Add network to the metamask. ( Network name - Localhost 7575, RPC URl - http://localhost:7545, Chain ID - 1337, Currency symbol - ETH)

Open MySQL and create database named voter_db. (DON'T USE XAMPP)

In the database created, create new table named voters in the given format and add some values.

    CREATE TABLE voters (
    voter_id VARCHAR(36) PRIMARY KEY NOT NULL,
    role ENUM('admin', 'user') NOT NULL,
    password VARCHAR(255) NOT NULL
    );

Install truffle globally

npm install -g truffle

Go to the root directory of repo and install node modules

npm install

Install python dependencies

pip install fastapi mysql-connector-python pydantic python-dotenv uvicorn uvicorn[standard] PyJWT

Usage
Note: Update the database credentials in the ./Database_API/.env file.

Open terminal at the project directory

Open Ganache and it's development workspace.

open terminal in project's root directory and run the command

 truffle console

then compile the smart contracts with command

 compile

exit the truffle console

Bundle app.js with browserify

 browserify ./src/js/app.js -o ./src/dist/app.bundle.js

Start the node server server

 node index.js

Navigate to Database_API folder in another terminal

 cd Database_API

then start the database server by following command

 uvicorn main:app --reload --host 127.0.0.1

In a new terminal migrate the truffle contract to local blockchain

 truffle migrate

You're all set! The Voting app should be up and running now at http://localhost:8080/.
For more info about usage checkout YouTube video.
