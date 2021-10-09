# Node StreamElements Info
Retrieving StreamElements information made easy.

# Installation
```npm
npm install streamelements-info
```
or clone the repository...

# Usage
```js
const streamElementsInfo = require('streamelements-info');

//Get channel ID and other data
streamElementsInfo.GetChannelData('gaules').then(channelData => {
	console.log(`\n=== Channel Data ===\n`);
	console.log(channelData);
	console.log(`\n====================\n`)
}).catch(error => {
	console.log(error);
});

//Get user loyalty points by using channel ID (get the ID from "GetChannelData")
streamElementsInfo.GetLoyaltyPoints('5cc799026e852d26fcf16717', 'naoconhecido').then(loyaltyPointsData => {
	console.log(`\n=== Loyalty Points Data ===\n`);
	console.log(loyaltyPointsData);
	console.log(`\n===========================\n`)
}).catch(error => {
	console.log(error);
});

//Get channel loyalty data by using channel ID (get the ID from "GetChannelData")
streamElementsInfo.GetLoyaltyData('5cc799026e852d26fcf16717').then(loyaltyData => {
	console.log(`\n=== Loyalty Data ===\n`);
	console.log(loyaltyData);
	console.log(`\n====================\n`)
}).catch(error => {
	console.log(error);
});

//Get channel loyalty store items by using channel ID (get the ID from "GetChannelData")
streamElementsInfo.GetLoyaltyStoreItems('5cc799026e852d26fcf16717').then(loyaltyStoreItems => {
	console.log(`\n=== Loyalty Store Items ===\n`);
	console.log(loyaltyStoreItems);
	console.log(`\n===========================\n`)
}).catch(error => {
	console.log(error);
});
```