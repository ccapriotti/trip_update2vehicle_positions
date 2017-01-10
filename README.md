"Why, what, how ? Not necessarily in that order."

This is a playground, with toys and rides. I may or may not finish this one 
day, but Iĺl leave it here for reference. You never know when your notes may
help someone.

My objective here was to create a simple way to convert a GTFS Realtime 
Trip Update feed (for short Iĺl refer to those as "GTFS-RT" and "TU") into a
fake Vehicle Positions (VP) feed, based on the static feed (AKA GTFS feed).

"WHY, oh WHY ?" you will ask, and probaby, next, you will also ask "how ?".

Well, besides the "palyground" answer, where I have fun, there is also another
reason. Sometimes you want to SEE where your vehcles are supposed to be,
claim to be, or are PREDICTED to be, or simply check where they were supposed 
to check in and never did.

If you are following me, I want to see where GPS or GPRS communication breaks,
while being able to create a heat map of where routes/trips are reported.

If this project ever gets published, it will (try) to use the One Bus Away
GTFS realtime visualizer as the plotting engine. 
(https://github.com/OneBusAway/onebusaway-gtfs-realtime-visualizer)




Now to the tech stuff you should know

This was developed in Python 2.7, on Ubuntu (16.04). 


The GTFS-RT OFFICIAL reference: 
https://github.com/google/transit/blob/master/gtfs-realtime/spec/en/reference.md

If you are familiar with protocol buffers, good for you, but if you are not,
do not spend too much time on the generic PB stuff. There is a specific part 
on protobuffs for Transit Realtime. You will not create, expand, or play 
around too much with the structure of protobuffs. 

Generic Python PB stuff:
https://developers.google.com/protocol-buffers/docs/pythontutorial

Sample Python GTFS-RT stuff:
https://developers.google.com/transit/gtfs-realtime/examples/python-sample


Pre-req: you absolutely must have protoc, which is part of the 
Google Protobufer suit. It is highly recommended that you match
its version with the protobuffer package you have. Please refer to Google's 
specific documentation. I suggest you compile protoc from the sources. 
It is easy.

Having protoc installed, have to compile the .proto file and that will 
generate the gtfs_realtime_pb2 referred on the code.
(Again, https://developers.google.com/protocol-buffers/docs/pythontutorial)


Only then you will be ready to play.


