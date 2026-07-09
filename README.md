Calendar = 
VAR BaseCalendar = CALENDARAUTO() 
RETURN 
ADDCOLUMNS( 
    BaseCalendar, 
    "Year", YEAR([Date]), 
    "Quarter Number", QUARTER([Date]), 
    "Quarter", "Q" & QUARTER([Date]), 
    "Month Number", MONTH([Date]), 
    "Month Name", FORMAT([Date], "MMMM"), 
    "Month Short", FORMAT([Date], "MMM"), 
    "Year Month Key", INT(FORMAT([Date], "YYYYMM")), 
    "Day of Week Number", WEEKDAY([Date], 2), 
    "Day Name", FORMAT([Date], "dddd") 
)
