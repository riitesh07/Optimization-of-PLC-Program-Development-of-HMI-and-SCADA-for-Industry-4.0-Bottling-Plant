# Optimization of PLC Program Development of HMI and SCADA for Industry 4.0 Bottling Plant  

A lab-scale industry 4.0 plant is a type of production model incorporating new integrated technologies currently being used in the industry.  

Overall Idea:  
This system can combine two different types of liquids depending on the customer’s requirements. When a customer places an order for a mixture of both liquids via a mobile app or an online portal, the liquid mixture must be filled accordingly.
Customer orders are generated and stored, which will process this data and it will be stored in a cloud. Following the generation of the order, the production process begins by placing an empty bottle on the conveyor belt with the help of a robot.
The robotic arm moves an empty bottle from a storage rack over an RFID scanner. The RFID chip is attached to the bottles. This is an indication of the beginning of the process. 
Then bottle is placed onto the conveyor. The bottle is moved to the fluid-filling plant by the conveyor belt and detected by a proximity sensor. The fluid-filling plant is a Festo compact workstation. 
A flow meter is used to control the amount of liquid that is poured into the bottles. After filling the bottles, they are transferred to a quality control station which is detected by another proximity sensor.
Bottles regardless of quality, are moved to a capping station, where the filled bottles are automatically capped. Then, OK-filled bottles are transported to the delivery point and NOT-OK are discarded.  

PLC IEC-61131-3 programming languages are being used such as,  
- ST - Structured Text (S7-SCL)
- FBD - Function Block Diagram
- LD - Ladder Diagram

CPU : Siemens S7-1212C AC/ DC/ Rly  
HMI : HMI KTP700 Basic PN  
SCADA : Ignition SCADA Software    

  ![WhatsApp Image 2024-02-23 at 12 07 44 PM (2)](https://github.com/riitesh07/Optimization-of-PLC-Program-Development-of-HMI-and-SCADA-for-Industry-4.0-Bottling-Plant/assets/68095076/a432f7f1-8505-4826-a81c-531804fc5610)  

  ![WhatsApp Image 2024-02-23 at 12 07 49 PM (2)](https://github.com/riitesh07/Optimization-of-PLC-Program-Development-of-HMI-and-SCADA-for-Industry-4.0-Bottling-Plant/assets/68095076/039eb1e6-b7c3-4a99-80d5-b2da756f656b)  

    



Control Code:  

- Main [OB]

    ![Screenshot (79)](https://github.com/riitesh07/Optimization-of-PLC-Program-Development-of-HMI-and-SCADA-for-Industry-4.0-Bottling-Plant/assets/68095076/164c627d-0154-49f3-a599-db6c9b10276f)

    ![Screenshot (80)](https://github.com/riitesh07/Optimization-of-PLC-Program-Development-of-HMI-and-SCADA-for-Industry-4.0-Bottling-Plant/assets/68095076/17d27bc2-b8d8-48ac-834d-347b2ef3db94)

    ![Screenshot (81)](https://github.com/riitesh07/Optimization-of-PLC-Program-Development-of-HMI-and-SCADA-for-Industry-4.0-Bottling-Plant/assets/68095076/766b183b-66a4-41c2-b916-31f0b1c8ab44)

    ![Screenshot (82)](https://github.com/riitesh07/Optimization-of-PLC-Program-Development-of-HMI-and-SCADA-for-Industry-4.0-Bottling-Plant/assets/68095076/548b9a6e-fa72-46a0-8378-7a5b700444b9)

    ![Screenshot (83)](https://github.com/riitesh07/Optimization-of-PLC-Program-Development-of-HMI-and-SCADA-for-Industry-4.0-Bottling-Plant/assets/68095076/11d7532d-fec9-41e8-852f-a95c0eaf0a8d)

    ![Screenshot (84)](https://github.com/riitesh07/Optimization-of-PLC-Program-Development-of-HMI-and-SCADA-for-Industry-4.0-Bottling-Plant/assets/68095076/6bd149a8-cbd3-46e6-943c-b3c862a2034a)

    ![Screenshot (85)](https://github.com/riitesh07/Optimization-of-PLC-Program-Development-of-HMI-and-SCADA-for-Industry-4.0-Bottling-Plant/assets/68095076/6f289ea4-7fd2-469a-8858-c9f012ec135f)

- Refilling Logic [FB]

    ![Screenshot (86)](https://github.com/riitesh07/Optimization-of-PLC-Program-Development-of-HMI-and-SCADA-for-Industry-4.0-Bottling-Plant/assets/68095076/d80a50de-44f3-4125-ae41-47d42c31d69c)

- Calculate operation time for One bottle and counting the total bottles

    ![Screenshot (87)](https://github.com/riitesh07/Optimization-of-PLC-Program-Development-of-HMI-and-SCADA-for-Industry-4.0-Bottling-Plant/assets/68095076/c28de605-d430-441a-8f42-c58933ccf59e)

    ![Screenshot (88)](https://github.com/riitesh07/Optimization-of-PLC-Program-Development-of-HMI-and-SCADA-for-Industry-4.0-Bottling-Plant/assets/68095076/af2ff5a5-192e-44f6-adae-b120d3294753)

- Filling process from Tanks

    ![Screenshot (89)](https://github.com/riitesh07/Optimization-of-PLC-Program-Development-of-HMI-and-SCADA-for-Industry-4.0-Bottling-Plant/assets/68095076/c5061975-7384-465b-90d1-1c3071079b30)

    ![Screenshot (90)](https://github.com/riitesh07/Optimization-of-PLC-Program-Development-of-HMI-and-SCADA-for-Industry-4.0-Bottling-Plant/assets/68095076/a06ed838-40b0-4cca-8354-441a2ab3120a)

- Production Data Reset

    ![Screenshot (91)](https://github.com/riitesh07/Optimization-of-PLC-Program-Development-of-HMI-and-SCADA-for-Industry-4.0-Bottling-Plant/assets/68095076/866817d3-fa3f-41c4-95e6-785aeaa749a1)

- PID Controller

    ![Screenshot (92)](https://github.com/riitesh07/Optimization-of-PLC-Program-Development-of-HMI-and-SCADA-for-Industry-4.0-Bottling-Plant/assets/68095076/06568523-f6c7-473e-bcc1-6a8341ed8f72)

HMI:  

- Root Screen

    ![Screenshot (95)](https://github.com/riitesh07/Optimization-of-PLC-Program-Development-of-HMI-and-SCADA-for-Industry-4.0-Bottling-Plant/assets/68095076/ca05cf98-4755-4688-947e-0db44d7c2e71)

- Different Jobs

   ![Screenshot (93)](https://github.com/riitesh07/Optimization-of-PLC-Program-Development-of-HMI-and-SCADA-for-Industry-4.0-Bottling-Plant/assets/68095076/b6003129-8611-4d56-8960-0695758f7551)

- Visualization Screen

   ![Screenshot (94)](https://github.com/riitesh07/Optimization-of-PLC-Program-Development-of-HMI-and-SCADA-for-Industry-4.0-Bottling-Plant/assets/68095076/04d2b3ee-2a66-4aa6-a183-1c374ca9f6ad)

    



















