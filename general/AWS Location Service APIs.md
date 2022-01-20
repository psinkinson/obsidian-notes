

DONE
====

BatchPutGeofenceCommand
- Adds a geofence to the GeofenceCollection in the Location Service
- Called when the Location DynamoDB table is updated
- Called very infrequently. i.e. when we get a list of plants from an RMC, or when an admin user edits a geofence shape
- Current Batch size = 1. (Max Batch size = 1,000)

BatchUpdateDevicePositionCommand
- Sends a lat/lng for a deviceId to the Tracker in the Location Service
- Called frequently. Each Truck location is updated every 10 seconds
- Current Batch size = 50. (Max Batch size = 10,000)

TODO
====

CalculateRouteCommand
- Assumption: Called once per incoming RMC Docket
- Assumption: We store route details response in Dynamo against the docketId to be used by frontend and any other part of the system 

UNKNOWN
=======

We are curently using Google maps. Unsure if we will stay with this or move to AWS Maps service.

# GeoCoordinates
Amazon Location Service accepts location data up to six decimal places of precision (0.000001), which equals to approximately 11 cm or 4.4 inches at the equator.
[Location FAQs](https://aws.amazon.com/location/faqs/)