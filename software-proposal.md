# **7.0 Software Implementation**

The software diagram provides a clear representation of how our software will function in order to meet the user needs and product requirements. The main loop of the software is responsible for the initialization, interrupt enable, and the logic of the code. The temperature sensor is used to measure the temperature and if it reaches 25°C or less, the motors/brushes are activated to start the cleaning process. Motor 1 is used to brush vertically to clean the solar panel and motor 2 to return the brush to its original place. This functionality satisfies the user needs by providing a self-cleaning mechanism that depends on the environmental reading that can keep the solar panels clean and improve their efficiency. Additionally, the software meets the product requirements by automating the cleaning process and eliminating the need for manual cleaning therefore decreasing the cleaning cost on the user.

During the design and decision-making process for the software, our team focused on simplicity and efficiency. We designed a simple loop that could effectively measure the temperature and control the motors based on the temperature readings. We also ensured that the software could be easily updated and modified to meet any future needs.

The Top 5 biggest changes to our software design since the software proposal are:

1. Implementation of Interrupts: We realized that using interrupts would allow for more efficient and accurate temperature measurements and user interface. This change allowed us to improve the overall performance of the system.

2. Use a simpler Algorithm: We simplified our software algorithm to make the programming more efficient and easy to understand by the user.

3. Implementation of Error Handling: We included error handling routines in the software to ensure that any errors that occurred during the operation of the system would be detected and handled appropriately.

4. Integration of PID Controller: We integrated a PID controller into our software to improve the accuracy and stability of the temperature control.

5. Implementation of Sleep Mode: We implemented a sleep mode feature  for 12 hours after each cleaning cycle to conserve power when the system is not in use. 

If we were to create a "Version 2.0" of our software design, we would focus on improving the overall efficiency and functionality of the system. One potential improvement would be to implement machine learning algorithms that could analyze the temperature and weather patterns to optimize the cleaning schedule. We could also improve the debuggability of the system by adding more comprehensive error-handling routines and integrating debugging tools. Additionally, we could incorporate more advanced peripherals and system features to make the system more reliable, stable, functional, and robust. For example, we could include sensors to detect when the solar panels are dirty, and automatically trigger the cleaning process. We can also use the voltage produced from the solar panel to indicate day and night time. Overall, these improvements would help us to create a more efficient and effective self-cleaning solar panel system. 



<figure class="image">  

<div style="text-align: center">  

<img src="images/soft.png" width="100%"><br>  

Figure 22 - Software proposal  

</div>

</figure>

