
Mark down file for writing and editting pseudo code, implementing algorithims, and planning.
# Sales Processign Module TO:DO
 - detailed problem decom & analysis
 - identify modules
 - detailed flowchart 
 - modular pseudocode

## Program Decomposition and Analysis
- Accept product ID and quantity
- check if we have engough inventory for the purchase
- calculate and apply discouont if product quantity is oveer 5 
- calculate the total of all the items
- adjust inventory accordingly
- maintain a record of the current purchase item and the price 
- display 'out of stock' if product quantity being purchased is more than on-hand inventory
- display the receipt of the purchase 
- display the total
(under the assumption that the product ID is always valid and the quantity is never negative)

## Modules
- Sales module 
    - Runs the initial program, including getting inputs for quantities, and the product Id's.
    - Call on other modules when necessary
- Inventory module
    - Checks if the product if in inventory and adjusts the currently inventory to reflect the purchase of the item
- Discount module
    - Checks of the quantity if over 5 and returns a discount amount
- Receipt
    - Maintains lists of the product ID's, the quantities, which will be used later to display the bill
- display bill 
    - Calls on Receipt moudule and displays the bill for the customer

## variables in use:
productID- id of the product
quantity- quantity the customer wants to purchase
productInventory - inventory of the product in the system
total -price after discount
discount- amount of discount added 
itemPrice - price per unit


## Draft 1 for pseudocode (without the modules)
START
DECLARE subtotal = 0
DECLARE total = 0
DECLARE bill = 'continue'
DECLARE itemID = []
DECLARE itemquantity = []
DECLARE itemprice =[]
WHILE bill == 'continue'
    INPUT productID
    INPUT quantity
    IF quantity < productInventory
        subtotal = quantity*itemPrice
        IF quantity > 5
            discount = total * .10
            subtotal = subtotal - discount
        END IF
        total = total + subtotal
        productInventory = productInventory-quantity
        itemID[length(itemID+1)] = productID
        itemquantity[length(itemquantity+1)] = quantity
        itemprice[item(itemqquantity+1)] = itemprice      
    ELSE
        DISPLAY "Out of Stock"
    ENDIF
    INPUT bill 'press continue to enter next item, or 'bill' for the receipt. 
END WHILE

FOR 0 to length of itemID
    DISPLAY itemID[i] , itemquantity[i], itemprice[i]
END FOR
DISPLAY total
END
