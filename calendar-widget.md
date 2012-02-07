Mini calendar widget
====================

Description
-----------
There is a bigger web application in development which needs a widget which renders a dynamic calendar into a given DOM element.

The calendar has to render the current month by default, and highlight the current day.    
The name of the current month plus the current year have to be shown in the header of the calendar.    
The names of the weekdays have to be displayed in short form above each calendar column.    

A few layout examples:    
http://365psd.com/day/2-122/    
http://365psd.com/day/2-152/    
http://365psd.com/day/2-252/    

The displayed month has to be switchable by the users to browse months in the future. Going back in time
is not desired - passed days should be in-active, too.    

The widget must be able to parse an array of event objects and render them into the calendar:

	[
		{
			time: 1328564770,
			event: "some event"
		},
		{
			time: 1328582356
			event: "another event"
		}
	]

Days with events have to be highlighted regardless of how many events occure on a single day. So the user
can only determine between days with events and days without events. The number of events is not of interest.

When the user clicks on a day, a custom callback function should be called, passing two parameters.    
First parameter: timestamp (UNIX) of the clicked day.    
Second parameter: Either an array of events happening at this day, or null.    


Its actually not clearly decided where exactly the calendar will be implemented. It could either be in 
a sidebar (250px width) or directly in the content area (600px width), so the calendar must adapt to the 
surrounding DOM element.    
The calendar must be fully styleable by CSS and must not break the surrounding styles of the application.

You can use any JS framework you want to solve this task.

----

Optional bonus points:

 * Make multiple, separate instances of the calendar possible.
 * Make the JSON data be updateable at any time.
 * Make the widget framework agnostic.
 * Create unit tests for the calendar widget.