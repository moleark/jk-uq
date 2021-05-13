订单的状态
=========

## ID
- OrderMain 
	- id
	- KEY no CHAR(20),
	- customer
	- sumQuanity 各行数量和
	- sumAmount 各行金额和
	- couponNo
	- index: customer-id
- OrderDetail
	- id
	- KEY master ID OrderMain,
	- KEY row SMALLINT,
	- product
	- pack
	- quantity
	- amount
	- price
## IDX
- DxOrderMainDraft
- DxOrderMainProcessing
- DxOrderDetailDelivered
- DxOrderDetailPaid
- DxOrderMainDone

