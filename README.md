# MClimate Vicki HomeAssistant connector
Connect the Lora Vicki radiator thermostat to HomeAssistant through Node-Red and Mqtt

![image](https://github.com/cnoork/MClimate_Vicki_HomeAssistant_connector/assets/17862084/70695931-71f3-4a5d-b74a-866ecc64c171)

To achieve the integration from the MClimate Vicki radiator themostat you need to have access and signal covarage from a Lora Wan server, a Node Red instance, a mqtt broker and the mqtt integration in Home Assistant to conennect the lora device to Home Assistant. Hereby you can receive updates from the sensors and actuators but also control actuators through Home Assistant manually and with automations. The developed solution is done with TTN (The Things Network) but could be changed to an other Lora servers with small adjustment.

I didn't had the need to make all posible switches available through HA, for instance switching "Child lock" "on/off" or changing temperature range and thereby not implemented.

When creating this solution there was not yet an encoder for downlinks available on the Lora server. In TTN is it possible to implement your own encoder/decoder. The used versions are added in the files (decoder is a copy from MClimate). To prevent issues with mixed lora devices it is recomended to create a sepperate application on the lora server for the Vicki devices which needs to be integrated in Home Assistant.

![image](https://github.com/cnoork/MClimate_Vicki_HomeAssistant_connector/assets/17862084/0595ca10-368e-4bcf-9063-79ce06c05fd7)

![image](https://github.com/cnoork/MClimate_Vicki_HomeAssistant_connector/assets/17862084/68a6389c-9fd1-458f-aea6-843529e8c4ca)

![image](https://github.com/cnoork/MClimate_Vicki_HomeAssistant_connector/assets/17862084/978a7f0b-72a0-494a-a759-2f87e1e2a51f)

![image](https://github.com/cnoork/MClimate_Vicki_HomeAssistant_connector/assets/17862084/cf88deae-c716-48f9-82bf-d8c853aba88d)
