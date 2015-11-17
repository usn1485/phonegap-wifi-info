# Cordova WifiInfo Plugin

* License - The MIT License
* Test on Cordova 3.4.0

Copied from - https://github.com/companje/org.apache.cordova.wifiinfo

##Install Step (Cordova CLI)


## API

### Get WifiInfo

Retrieve the wifi information available from the last scan.  
(TODO: handle options to require a new scan and fresh data)

```javascript
navigator.wifi.getWifiInfo(success, error, options);
```

### Watch WifiInfo

Require a new wifi scan as soon as possible and
retrieve continuatively the obtained data.  
(TODO: handle options to enable/disable the scan request)

```javascript
id = navigator.wifi.watchWifiInfo(success, error, options);
```

### Clear Watch

Unwatch wifi updates

```javascript
navigator.wifi.clearWatch(id);
```

### On Success Data

```javascript
{
	connection: {
		BSSID: BSSID,
		HiddenSSID: HiddenSSID,
		SSID: SSID,
		MacAddress: MacAddress,
		IpAddressInt: IpAddressInt,
		IpAddress: IpAddress,
		NetworkId: NetworkId,
		RSSI: RSSI,
		LinkSpeed: LinkSpeed
	},
	
	networks: [
		{
			BSSID: BSSID,
			SSID: SSID,
			frequency: frequency,
			level: level,
			capabilities: capabilities
		},
		...
	]
}

