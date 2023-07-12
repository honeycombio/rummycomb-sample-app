# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

And then it was modified to send data to Honeycomb, according to the [docs](https://docs.honeycomb.io/getting-data-in/opentelemetry/browser-js/). We initialized tracing [in tracing.js[(https://github.com/jessitron/from-rum-to-honeycomb/blob/847d9223dae205691c69aa0d06438ab467c72eb5/src/tracing.js), imported that in [App.js](https://github.com/jessitron/from-rum-to-honeycomb/blob/847d9223dae205691c69aa0d06438ab467c72eb5/src/App.js#L1C19-L1C19), and set up an environment variable in [.env](https://github.com/jessitron/from-rum-to-honeycomb/blob/847d9223dae205691c69aa0d06438ab467c72eb5/.env)

To use this app:

1. Create an API key in Honeycomb with only permissions "Send data" and "Create dataset"
2. Put that in an environment variable:

`export HONEYCOMB_API_KEY=yourapikeyhere`

3. Run the app.
4. Go look at the 'browser' dataset in Honeycomb.

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes to App.js.\
You may also see any lint errors in the console.

### `npm run load`

This will run the exciting generate-load.js script. This opens localhost:3000 in a headless browser, waits 5-10 seconds, then does it again.

Run several of these at once to generate a reasonable amount of page loads. Then you can count those in Honeycomb!
