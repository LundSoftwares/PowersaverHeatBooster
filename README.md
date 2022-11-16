## This Node Red Subflow creates a "Booster sensor" to be used with the [Powersaver Nodes](http://www.powersaver.no) ##

If you want to boost the heater just before a longer OFF period, set your desired Offset and the output will give you a True value if "Start time for next OFF period" Minus "Time now" is within the offset, and the OFF period is equal or bigger than the Min OFF Hour value.

![image](https://user-images.githubusercontent.com/23386303/202223223-f9777574-fa58-46a2-98bb-349042f025ed.png)


**Example:** Next OFF period is 5 hours long and starts at 17:00, Offset and Min OFF hours is both is set to 3 hours. Between 14:00 and 17:00, the output is True, before and after the value is False. If the OFF period was only 2 hours long, the value will be Off all the time and no heater boost will be generated.

**How to:** Connect the Input to the Schedule Output on one of the Powersaver nodes (Lowest Price and Best Save only!) Set your desired offset and Min OFF Hours, default is 3 hours. Preferably connect the Output to a HomeAssistant Entity node set to Binary Sensor, this sensor can then be used as trigger for boosting you heater.

![image](https://user-images.githubusercontent.com/23386303/202222981-6a20b948-e03e-49f9-8dc6-661afe2993f7.png)
