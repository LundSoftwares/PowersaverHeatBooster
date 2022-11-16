This Subflow creates a "Booster sensor" to be used with the Powersaver Nodes.

In short: If you want to boost the heater just before a longer OFF period, set your desired Offset and the output will give you a True value if "Start time for next OFF period" Minus "Time now" is within the offset, and the OFF period is equal or bigger than the Min OFF Hour value.

Example: Next OFF period is 5 hours long and starts at 17:00, Offset and Min OFF hours is both is set to 3 hours. Between 14:00 and 17:00, the output is True, before and after the value is False. If the OFF period was only 2 hours long, the value will be Off all the time and no heater boost will be generated.

How to: Connect the Input to the Schedule Output on one of the Powersaver nodes (Lowest Price and Best Save only!) Set you desired offset and Min OFF Hours, default is 3 hours. Preferably connect the Output to a HomeAssistant Entity node set to Binary Sensor.
