
## Fulfillment EDI events
---
#### ShipmentDropshipAssigned
topic: shipment.dropshipassigned

#### ShipmentDropshipInvoiceReceived
topic: shipment.dropshipinvoicereceived

---

Those will include dropshipVendorId/Code

i can add a created event if preferred…

## Fulfillment APIs
#### Create shipment
- add support for specifying dropshipVendorId
- If dropshipVendorId missing from payload, get it from assigned location and then persist on shipment

Invoice - edi-810  ...new Fulfillment API /api/commerce/shipments/{shipmentNumber}/dropship/invoice-received

## Dropship BPM

Default_Dropship.bpmn
- basically a stripped down STH process

"Pre-ACK" script task
- PRE_ACKNOWLEDGEMENT

"Order Acknowledgement" user task   - edi-855
- support partial acknowledge by lineId and qty
- cancel remaining items if partial qty across items
- cancel shipment if no qty across items
- DROPSHIP_ORDER_ACKNOWLEDGED - workflow state on completion of task

"Prepare Shipments (ASN)" user task  - edi-856
- packages created
- items in boxes
- tracking numbers assigned
- COMPLETED - workflow state on completion of task

Support standard ops:
- CANCEL 
- CUSTOMER_CARE


