Dynamo table
https://eu-west-1.console.aws.amazon.com/dynamodbv2/home?region=eu-west-1#table?name=Production-DataStorage-Stack-augmentedlog6B4846BA-15J9I7UD422OI&tab=overview

Stream
https://eu-west-1.console.aws.amazon.com/firehose/home?region=eu-west-1#/details/augmented_log_delivery_stream

Log schema
https://github.com/CloudCycle/DataStorage/blob/main/common/augmented-log.ts

Current
rmc_provider = RMCProvider
run_id = 'live'
load_volume = 8
prediction_trip_posix_timestamp_start - needs to be +

// TRUCK STATE
  prediction_truckstate_current: string;
  prediction_truckstate_lastvalid: string; invalids have been filtered out