**Summary of Discussion**

- **Model and API Updates:** Tanmay updated contracts for a model changes ticket in the "Vendor Management and Adoption Fulfillment" epic. He confirmed that the `GET` invoice API needs to be updated to support searching and filtering by fields like invoice status, amount, and invoice number.
- **New Endpoint:** Kelly suggested, and Tanmay agreed to add, a `PATCH` endpoint to the invoice/payments API for additional CRUD operations.
- **Dropship Support:** Tanmay added an `isDropship` field to the shipment model contracts. Kelly is creating the necessary Business Process Model (BPM) to support the dropship flow, which will include tasks for Purchase Order Acknowledgment (EDI 855) and Advanced Shipping Notice (ASN) (EDI 856).
- **Dropship Logic:** The `isDropship` flag on a shipment should primarily be set by checking if the assigned location is a dropship location in the group configs.
- **Next Steps for PRs:** Tanmay was advised to send his existing pull request containing the contract updates for code review.
- **Upcoming Events:** Kelly confirmed that she will also add events, such as 'Dropship assigned' and 'Dropship created,' to the invoice events ticket (499) this week.
- **Issue Resolution:** Tanmay successfully fixed a concurrency issue in a previous sprint ticket that was causing tasks to take too long.

List key takeaways

**Key Takeaways and Decisions**

- Tanmay will submit his pull request with the updated model contracts, including the new
    
    ```
    isDropship 
    ```
    
    field for the shipment model, for code review.
- The
    
    ```
    GET 
    ```
    
    invoice API will be updated to support searching and filtering by invoice status, amount, and invoice number, and a
    
    ```
    PATCH 
    ```
    
    endpoint will also be added.
- Kelly will create the dropship Business Process Model (BPM) (including EDI 855 and ASN EDI 856 tasks), aiming to complete it by the end of the week.
- The logic for setting the dropship flag will rely on confirming that the shipment's assigned location is configured as a dropship location.
- Kelly will add 'Dropship assigned' and 'Dropship created' events to the existing invoice events ticket (499) this week.

**Action items**

- **Kelly Taylor:**
    - Create the Business Process Model (BPM) for the dropship flow, including the Purchase Order Acknowledgment (EDI 855) and Advanced Shipping Notice (ASN) (EDI 856) tasks, aiming to complete it by the end of the week.
    - Add the 'Dropship assigned' and 'Dropship created' events to the invoice events ticket (499).
- **Tanmay Bhabire:**
    - Send the pull request with the updated contracts for the shipment model (including the `isDropship` field) for code review.
    - Implement search/filtering for invoice number, status, and amount on the `GET` invoice API.
    - Add a `PATCH` endpoint to the invoice API.