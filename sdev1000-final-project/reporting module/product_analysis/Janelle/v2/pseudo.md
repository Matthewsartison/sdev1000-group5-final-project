
START FUNCTION build_product_and_quantities (rows)

    DECLARE product_quantities as empty dictionairy 

    FOR EACH row IN rows
        SET product_name = row["Product Name"]
        SET product_count = row["Quantity"]

        IF product_name exists in product_quantities THEN
            product_quantities[product_name] = product_quantities[product_name] + product_count
        ELSE
            product_quantities[product_name] = product_count
        ENDIF
    ENDFOR
    RETURN product_quantities
ENDFUNCTION

START FUNCTION product_and_quantities_list(dictionairy)
    SET list as empty list
    <!-- product name: quantity -->
    FOR EACH product, count IN dictionary
        ADD product, count TO list
    RETURN list

END FUNCTION

START FUNCTION display_products_by_choice (choice, list)
    IF choice = "Top 5" 
        DISPLAY "Top 5 products are: "
        SET last_row = length (list) - 1
        SET i = last_row
        SET counter = 0
        WHILE counter < 5
            DISPLAY list [i]
            SET i = i - 1
            counter = counter + 1
        ENDWHILE
        
    ELSE
        DISPLAY "Bottom 5 products are: "
        SET i = 0
        WHILE i < 5
            DISPLAY list [i]
            SET i = i + 1
        ENDWHILE
    ENDIF
ENDFUNCTION




START

SET rows = loadCSV()

SET product_totals_dictionairy = build_product_and_quantities(rows)

SET product_totals_list = product_and_quantities_list(product_totals_dictionary)

SORT product_totals_list ascending as sorted_list

INPUT "Top 5 or Bottom 5" as choice

display_products_by_choice(choice, sorted_list)

END

*TO DO ENSURE 0 index