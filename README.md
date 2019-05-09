# CSGO GOTV Broadcast sytem

This is a POC code to test the CSGO's [GOTV broadcast](https://developer.valvesoftware.com/wiki/Counter-Strike:_Global_Offensive_Broadcast) feature.  
Relays GOTV data as low-latency demo.  

## Usage
* `go run main.go`
    - This will start the webserver on port 3090 (will be configurable soon)
* Use something like ngrok to get a public endpoint 
    - `ngrok http 3090`
    - Say the endpoint is `http://SomeEndPoint.ngrok.io`
* On your CSGO server set
    - `tv_broadcast_url "http://SomeEndEndpoint.ngrok.io"`
    - `tv_broadcast 1`
* Currently use the logs from the webserver to figure out the token
* In your CSGO client use ` playcast "http://SomeEndPoint.ngrok.io/match/<token>"` to watch the broadcast 

## TODO
* Maintain releases
* Add flags to configure the server
