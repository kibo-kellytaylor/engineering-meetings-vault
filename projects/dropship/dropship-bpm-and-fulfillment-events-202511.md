
## Fulfillment EDI events
---
#### ShipmentDropshipAssigned
topic: shipment.dropshipassigned

#### ShipmentDropshipInvoiceReceived
topic: shipment.dropshipinvoicereceived

---

Those will include dropshipVendorId/Code

i can add a created event if preferred…


## Create shipment...add support for specifying dropshipVendorId/Code

...if missing?? call location service for vendor code and then persist on shipment


## Dropship BPM

...basically a trimmed down STH process...  Default_Dropship.bpmn


"Pre-ACK" script task

PRE_ACKNOWLEDGEMENT


"Order Acknowledgement" user task   - edi-850

ORDER_ACKNOWLEDGED - workflow state ...maybe just ACKNOWLEDGED
...support partial acknowledge 


"Prepare Shipments (ASN)" user task  - edi-855

COMPLETED - workflow state


CANCEL 
CUSTOMER_CARE


Invoice - edi-810  ...new Fulfillment API /api/commerce/shipments/{shipmentNumber}/dropship/invoice-received

