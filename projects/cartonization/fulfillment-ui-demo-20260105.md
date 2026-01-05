The discussion focused primarily on a demo of the **Fulfillment UI's packing recommendations** feature and a status update on **rate shopping**.

- Amol Shinde demonstrated the cartonization flow, including the use of recommended box types, a 3D packing view, and the error message received when an item is too large for the available box dimensions.
- It was confirmed that product dimensions are mandatory, and if they are missing, the system cannot generate packing recommendations for the shipment.
- The current Minimum Viable Product (MVP) optimization strategy for packing recommendations is based solely on maximizing **total volume utilization** in the available boxes.
- Future enhancements will introduce additional strategies, including optimization by the **lowest number of boxes** and **cost of the box**, which will be user-selectable in tenant settings.
- Amit Ugane requested an update on rate shopping, and Amit Solanki confirmed a demo is scheduled for tomorrow with Travis.
- Concerns were raised that recent changes to the contract required re-work, potentially impacting the 1/20 target for the rate shopping feature.


The key takeaways and decisions from the meeting are:

- The current Minimum Viable Product (MVP) for packing recommendations is built on a strategy focused solely on maximizing total volume utilization, not minimizing the number of boxes.
- The system requires complete product dimension data, and it was confirmed that if any items cannot be packed using the available box types, the system will not provide partial recommendations.
- A plan was made for an immediate follow-up to the MVP to enhance the packing recommendation feature by adding optimization strategies based on the lowest number of boxes and potentially cost.
- The team acknowledged the need to address a contract change that caused rework for the rate shopping feature and confirmed a demo for rate shopping is scheduled for tomorrow.

Action items

- **Aditi Sawant:**
    - Add the three cartonization strategies (total volume, number of boxes, and cost of box) to the epic tickets, specifying that total volume is for the first phase and the others will be covered in upcoming implementation.
- **Amit Solanki:**
    - Investigate the feasibility of combining the "least number of boxes" and "maximum volume utilization" strategies for packing recommendations.
- **Amol Shinde:**
    - Double-check if the system defaults to one inch for length, width, and height when a product's dimensions are not provided.
- **Group:**
    - Follow up with Srikanth and Travis tomorrow in the scheduled demo call to discuss the status of rate shopping, including open questions and the impact of the contract changes.
- **Madhulika Saxena:**
    - Perform a quality assurance check for the maximum weight allowed on a box in the packing recommendation feature.