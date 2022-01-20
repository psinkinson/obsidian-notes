# Existing code
https://github.com/CloudCycle/InternalOps/blob/main/lambda-fns/calibration/main.ts
adds a truck record, adds calibration record

# Deregister truck/device
- Remove "truck_registration" param from DeviceList table
- Delete row in Truck table
- Delete row in Calibration table
- Delete row with imei=device_id in TruckInformationSnapshot table
# Truck table
## fields
device_id, registration, rmc_provider

# Tokens table
## desc
quick lookup of IMEI



# DeviceList table
## desc
links registration and imei
## fields
imei, serial_no, truck_registration

