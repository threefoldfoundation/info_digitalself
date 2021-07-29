# Autopay

![](img/autopay.png)

Implemented in the Payment experience, Autopay allows Digital Twin Owners as consumers to specify which merchants they want to allow to ask for a payment. 

They can specify how much money can be spent on one or more merchants per period (can also be scheduled for multiple periods). This will enable the merchants to be paid as long as the spending limit is not reached.

Merchants need to specify transaction details while Digital Twin Owners have full oversight of the payments done. 

## Implementation 

The first version of Autopay will allow Farmers on the Threefold Grid to ask for payment for IT capacity used on the grid. 

Each Autopay entry has the following information: 
- X number of merchants who can ask for a payment 
    - Each merchant needs to be identified by an ID or a unique name. 
- Maximum amount of payment per period (Can also be scheduled for multiple periods)
    - Payment amount specified in chosen currency (For first version; EUR/USD/[TFT](token_what)/BTC)
- Optional secret for payment - Merchants needs to specify when they will ask for payment. 
- Minimal required reputation level - Not implemented yet.






