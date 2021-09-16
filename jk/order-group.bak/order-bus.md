# Order Bus 的流程

## Order UQ

- 发货：
    - deliver：应发数量
    - deliverDone：实发数量

- 现收：先收款，后发货
    - receive：应收。收款后记应收
    - receiveDone：实收。收款后同时记实收
    - 完成发货时，如果缺发，记退款

- 应收：先发货，后收款
    - receive：应收。deliver-done后记应收
    - receiveDone：实收。receive-done后记实收
    - 完成发货时，记应收

- 申请退货：
    - deliverReturn: 应退
    - deliverDone: 已退
    - receiveReturn：应退款
    - receiveReturnDone: 已退款
    - 接受退货申请时，记应退款
    - 退款完成时，记已退款

- 现场退货：
    - deliverReturn: 应退
    - deliverDone: 已退
    - receiveReturn：应退款
    - receiveReturnDone: 已退款

-----
## Receive UQ

- receive of jk-order bus
    - receive: 记应收

- receive-return of jk-order bus
    - return: 记应退

- receive 字段
    - receive: 应收
    - receiveDone: 已收
    - return: 应退
    - returnDone: 已退

