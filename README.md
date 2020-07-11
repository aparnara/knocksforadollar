# knocksforadollar

## How to run locally

1. Install Homebrew
    - Paste the following in a macOS Terminal prompt: 
      - */usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"*

2. Install Node via Homebrew
    - Paste the following in a macOS Terminal prompt: 
      - *brew install node*
    - Check the NPM version to confirm node and npm were installed by pasting the following in a macOS Terminal prompt: 
      - *npm -v*

3. Clone and configure the sample 
    - Paste the following in a macOS Terminal prompt: 
      - *git clone https://github.com/aparnara/knocksforadollar/*

4. Set up webhook integration using the Stripe CLI
    - First [install the CLI](https://stripe.com/docs/stripe-cli) and [link your Stripe account](https://stripe.com/docs/stripe-cli#link-account).
    - Run the following command:
      - *stripe listen --forward-to localhost:4242/webhook*
    - Set STRIPE_WEBHOOK_SECRET to value printed by CLI in your .env file below.
    
5. Set up .env
    - Rename the .env.example by pasting the following in a macOS Terminal prompt:
      - *mv .env.example .env*
    - Follow instructions in .env

4. Run the server and test
    - Paste the following in a macOS Terminal prompt:
      - *cd /server*
      - *npm install*
      - *npm start*
    - This should run the server, launch a browser and navigate to http://localhost:4242/ and test away. 
