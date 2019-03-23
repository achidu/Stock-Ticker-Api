# Stock-Ticker-App
A real-time stock ticker app built using Angular 

These are the main files I wrote using TypeScript, HTML, and CSS to create a functioning (on a local host) stock ticker api. 

First, there’s an API that loads current stock price data from Yahoo! Finance. It’s a standard REST API and doesn’t require authentication deployed on Heroku. I created a service to access and load data from the API.

When the app loads, it shows the dashboard page with a list of cards. Each card contains a single stock, the current price, and the day’s change in price (as a currency value and as a percentage). The background of the cards will be red for negative change, green for a positive change, or gray for no change. Each of these cards is an instance of a component that takes the stock data and determines how to render the card.

The top navbar has two links, to the dashboard and manage views, which allow for general navigation between the views. I use the Angular Router to set up these routes and manage how the browser determines which to display.

When you click the Manage link in the navbar, you’ll see the manage page with a list of the stocks. Here you can remove any of the stocks by clicking the Remove button. You can also add new stocks by typing the stock symbol into the text area and pressing the Enter key.

The form is updated immediately upon changes input by the user. The list can be extended by putting a new stock symbol in the input field and hitting Enter, or the list can be reduced by clicking the Remove button. In both cases, the list of symbols is immediately changed, and if you go back to the dashboard you’ll see the updated list appear.

Note: The app is not persistent
