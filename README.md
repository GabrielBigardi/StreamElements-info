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
streamElementsInfo.GetChannelData('naoconhecido').then(channelData => {
	console.log(channelData);
}).catch(error => {
	console.log(error);
});

//Get user loyalty points by using channel ID (get the ID from "GetChannelData")
streamElementsInfo.GetLoyaltyPoints(channelData._id, 'gaules').then(loyaltyPointsData => {
	console.log(loyaltyPointsData);
}).catch(error => {
	console.log(error);
});

//Get channel loyalty data by using channel ID (get the ID from "GetChannelData")
streamElementsInfo.GetLoyaltyData(channelData._id).then(channelLoyaltyData => {
	console.log(channelLoyaltyData);
}).catch(error => {
	console.log(error);
});

//Get channel loyalty store items by using channel ID (get the ID from "GetChannelData")
streamElementsInfo.GetLoyaltyStoreItems(channelData._id).then(channelLoyaltyData => {
	console.log(channelLoyaltyData);
}).catch(error => {
	console.log(error);
});
```