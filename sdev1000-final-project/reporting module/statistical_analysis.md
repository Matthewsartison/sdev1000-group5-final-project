START
//FUNCTIONS

TOTAL REVENUE CALCULATOR
FUNCTION calculateTotalRevenue(dataToCalculate)
    SET sum = 0
    SET count = 0 
    FOR value in loadSalesData(dataToCalculate):
        sum+=value
        count+=1 // variable kept in place incase we want to calculate average
    END FOR
    RETURN sum, count
END FUNCTION


AVERAGE CALCULATOR

FUNCTION calculateAvgerage(dataToCalculate)
    DECLARE average
    calculateTotalRevenue(dataToCalculate)
    IF count > 0 THEN:
        averageTransaction = sum/count       
    ELSE THEN:
        aveargeTransaction = 0
    ENDIF
    RETURN f'Average transaction value for {dataToCalculate} is: {averageTransaction}
END FUNCTION




DECLARE dataInput
DECLARE menu = True  
WHILE True
    menuChoice = INPUT
                        """
                        MENU OPTION:
                        1. Calculate Total
                        2. Calculate average
                        3. QUIT
                        WHICH CALCULATION WOULD YOU LIKE TO PREFORM (1/2/3): 
                        """
    IF menuChoice IS '1' THEN:
        DECLARE selectedData
        selectedData = INPUT "What data would like the total for?: " 
        IF selectedData IN sales_data.csv AND IS type(INT) THEN:
            calculateTotalRevenue(selectedData) // will return sum and count
            PRINT sum
        ELSE THEN:
            PRINT "DATA NOT FOUND, PLEASE TRY AGAIN"
        ENDIF
    IF menuChoice IS '2' THEN:
        DECLARE selectedData
        selectedData = INPUT "what would you like the average of?: "
        IF selectedData IN sales_data.csv AND is type(INT) THEN:
            calculateAvgerage(selectedData)
            PRINT f"the average of {selectedData} is: {averageTransaction}
        ELSE THEN:
            print "DATA NOT FOUND, PLEASE TRY AGAIN"
        END IF
    ELSE IF menuChoice IS '3' THEN:
        menu = False
        PRINT 'PROGRAM EXITED'
    END IF
END WHILE
