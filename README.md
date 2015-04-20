# SparkCore-Api-via-MaxMsp

simple method to get your awesome internet sensor in to Maxmsp

/*Sparkcore-bug Code */

int analog0 = 0; int analog1 = 0; void setup() { Spark.variable("analog0", &analog0, INT); pinMode(A0, INPUT); Spark.variable("analog1", &analog1, INT); pinMode(A1, INPUT); }

void loop() { analog0 = analogRead(A0); analog1 = analogRead(A1); }

then edit patch with your data

and

You can now make a GET request with your terminal or browser like

EXAMPLE REQUEST IN TERMINAL
Core ID is YOUR-ID-01234567
Your access token is 1234123412341234123412341234123412341234
curl "https://api.spark.io/v1/devices/YOUR-ID-01234567/temperature?access_token=1234123412341234123412341234123412341234"

And the response contains a result like this:

// EXAMPLE RESPONSE { "cmd": "VarReturn", "name": "temperature", "result": 2342, "coreInfo": { "last_app": "", "last_heard": "2014-08-22T22:33:25.407Z", "connected": true, "deviceID": "YOUR-ID-01234567" }

