# to-do-list

Enhancement of the template to-do application with additional features.

## Addition of Date Added

The application now displays the date that the to-do item is added to the list. This is accomplished by importing the date module and calling the date.today() function to obtain the current date. This value is obtained when a POST request is sent to '/add'. A new column is also added to the SQL database to hold the value of today's date so that it can be passed on to the HTML file.

## Addition of Date/Time Completed

The application now displays the date and time that the to-do item is completed. This is accomplished by importing the datetime module and calling the datetime.now() function to obtain the current date and time. This is then converted to text by calling strftime("%Y-%m-%d %H:%M:%S"). A new column is added to the SQL database to hold the value of today's date and time so that it can be passed on to the HTML file. This value has to be defined as nullable=True (don't know why).

## Removal of Toggle Option

No longer can an item be toggled from "complete" to "pending." This is accomplished by placing a conditional that allows the change only if the value of "completed" is false. The time stamp occurs within this conditional statement so that the time cannot be updated.

## Removal of Completed Anchor Tag

Using a conditional within the HTML document, once a task is completed, the status "completed" is no longer a link that can be clicked.
