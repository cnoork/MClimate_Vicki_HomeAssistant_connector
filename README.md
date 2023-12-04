# MClimate Vicki HomeAssistant connector
Connect the Lora Vicki radiator thermostat to HomeAssistant through Node-Red and Mqtt

https://mclimate.eu/products/vicki-lorawan

![image](https://github.com/cnoork/MClimate_Vicki_HomeAssistant_connector/assets/17862084/70695931-71f3-4a5d-b74a-866ecc64c171)

To achieve the integration from the MClimate Vicki radiator themostat you need to have access and signal covarage from a Lora Wan server, a Node Red instance, a mqtt broker and the mqtt integration in Home Assistant to connect the lora device to Home Assistant. Hereby you can receive updates from the sensors and actuators but also control actuators through Home Assistant manually and with automations. The developed solution is done with TTN (The Things Network) but could be changed to any other Lora Wan servers but needs probably some small adjustments.

I didn't had the need to make all posible switches available through HA, for instance switching "Child lock" "on/off" or changing temperature range are thereby not implemented.

When creating this solution there was not yet an encoder for downlinks available on the Lora server. In TTN is it possible to implement your own encoder/decoder. The used versions are added in the files (decoder is a copy from MClimate). To prevent issues with mixed lora devices it is recomended to create a sepperate application on the Lora Wan server for the Vicki devices which needs to be integrated in Home Assistant.

![image](https://github.com/cnoork/MClimate_Vicki_HomeAssistant_connector/assets/17862084/0595ca10-368e-4bcf-9063-79ce06c05fd7)

Dashboard example:

![image](https://github.com/cnoork/MClimate_Vicki_HomeAssistant_connector/assets/17862084/68a6389c-9fd1-458f-aea6-843529e8c4ca)

Available properties for automation:

![image](https://github.com/cnoork/MClimate_Vicki_HomeAssistant_connector/assets/17862084/978a7f0b-72a0-494a-a759-2f87e1e2a51f)

For connection with mqtt from TTN you can use "mqtts://eu1.cloud.thethings.network" or "mqtt://eu1.cloud.thethings.network" as address and for user "\<your application name\>@ttn" and the password is a generated API key from TTN.

![image](https://github.com/cnoork/MClimate_Vicki_HomeAssistant_connector/assets/17862084/d11eefb5-414a-40cb-b67c-4cd35b47f823)

All functions with multiple outputs is the first one for debug with all input and output info.
