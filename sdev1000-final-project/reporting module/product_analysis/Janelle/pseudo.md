START
 

--------FUNCTIONS------

function getHeaders () {
	SET headers = []
	FOR item IN row[0]:
		ADD item to headers
	ENDFOR
	RETURN headers
}

function targetColumnLocation (target_column_name, item_list) {
	count = 0
	FOR item IN item_list
		IF item == target_column_name
			RETURN item_list[count]
		ENDIF
		SET count = count+1
	ENDFOR
}

function buildProductTotalsList (choice) {
	IF choice == product_name OR choice == product_id
		DISPLAY "Invalid"
	IF choice IN headers:
		SET choice_list = []
		FOR product IN product_name_column
			SET choice_total = 0
			SET choice_total = choice_total + product_(choice)
			ADD (product, choice_total) TO choice_list
		ENDFOR
		RETURN choice_list
	ELSE:
		THROW error (?)
	ENDIF
}



function displayRankedResults (choice_list, popularity_choice) {
	
	IF popularity_choice == "Top 5":
		SORT choice_list in descending order by choice_total
		DISPLAY "Top 5 products by {choice}"
	ELSE IF popularity_choice == "Bottom 5":
		SORT choice_list in ascending order by choice_total
		DISPLAY "Bottom 5 products by {choice}"
	ELSE:
		RETURN "Invalid"
	END IF

	SET count = 0
	WHILE count < 5
		DISPLAY "(count+1). choice_list[count]"
		SET count as count + 1
	END WHILE
}

----------MAIN----------

loadCsv("sales.csv")

SET headers = getHeaders()

SET product_name_column = targetColumnLocation (product_name, headers)

INPUT "Top 5 or Bottom 5?" AS popularity_choice
INPUT "By which column?" AS choice

SET choice_list =  buildProductTotalsList (choice)

DISPLAY displayRankedResults (choice_list, popularity_choice)


END