

Mark down file for writing and editting pseudo code, implementing algorithims, and planning.


START

DECLARE Dictionary storeInventory = {}
#Needs ProductID
DECLARE productNumber =
#Needs productName
DECLARE productName = INPUT
#Needs Category
categoryGrocery = G
categoryHealth = H
categoryMisc = M
# Needs Price
Price = positive decimal

#Validate inputs



#productName is not empty
FUNCTION productNaming()
	productName = INPUT(Please enter a valid product name. With no symbols."
		IF productName == "" 
			DISPLAY(f"{productName) saved!
			RETURN productName
		ELSE
			DISPLAY(ERROR: inavlid name. No symbols are allowed, only letters A-Z)
		ENDIF
ENDFUNCTION


#category is not empty
FUNCTION categoryDefine()
	productCategory = INPUT("Please enter a valid product letter identifer. Must include a valid section identifer. (G, for Grocery, H for Health, M for Misc)")
		IF productCategory == ("G" OR "H" OR "M") OR productCategory LENGTH > 1
			THEN RETURN productCategory
		ELSE
			DISPLAY(ERROR: invalid category code. Must include uppercase G for Grocery, H for Health or M for MISC.)
		ENDIF
ENDFUNCTION



#productId is unique and alphanumeric
FUNCTION addProductId()
	productNumber = INPUT ("Please enter a valid ProductNumber. MUST include 4 integers.")
		IF productNumber == LENGTH(4) AND productNumber==integer
			THEN productId =( productNumber + productCategory)
			RETURN productID
		ELSE 
			DISPLAY("ERROR: productID is invalid. MUST include 4 integers."
		ENDIF
ENDFUNCTION

END

<!-- •	Accept inputs for adding new products with the following fields: 
o	Product ID (Unique identifier, alphanumeric) 
o	Product Name (String) 
o	Category (String, e.g., Electronics, Clothing, Books, etc.) 
o	Price (Decimal, representing the price of the product) 
o	Quantity (Integer, representing stock level)  -->


