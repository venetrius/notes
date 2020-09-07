# Adapter Pattern

# Used if an output of system A is not compatible with the expected input of system b

# structure
- client A who want to use
- adaptee B  which want to be used
- target interface C describes the API called by the client A
- adapter D implements the interface C which will be used by the client A to access adaptee B

# specific example
webClient calling webService
client want to send object
server only accepts json (request(Json): Json)
Interface => webRequester (request(Object): int)
WebAdapter (request(Object): int; connect(WebService):void; toJson(Object):json)

