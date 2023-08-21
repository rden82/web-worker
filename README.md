# WebWorker

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 16.2.0.

## Development server
Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The application will automatically reload if you change any of the source files.

## Task
Create a SPA application that receives large amounts of data with high frequency. The data should be received in the web-worker from a pseudo-socket and passed to the main thread. The main thread should render the incoming data in the amount of the last 10 elements.

## Requirements:
1.	Make a pseudo-socket through a timer. Take into account the ability to change the value of the timer interval through the UI (input), in ms
2.	The size of the data array coming from the pseudo-socket can be adjusted via the UI (input)
3.	A single array element is an object that has the following fields:
    * id - string field
  	*	int - integer field
  	*	float - float field (precision === 18)
  	*	color - string field with color name (can be in any representation rgb, hex, string)
  	*	child - field which is an object that has two fields - id and color
5.	Only the last 10 elements will be displayed in the UIa and may contain their own set of ids, which can be set in the UI. For example, 1000 items come from the thread. Of these, 10 elements are selected for display as specified in the task. If additional_ids are set, the IDs are overwritten for the first elements of these 10 elements.
6.	In the main thread, you need to use not raw objects, but classes that are created based on the models described in step 3
7.	In the UI, it is required to display data in the following representation:
    * each element is a table row
    * fields are columns
    * child is a nested table

When rendering the color column, it is necessary to fill its background with the color specified in the field

## Technologies and libraries:
1.	angular 15
2.	web-worker
3.	jest || jasmine+karma

## The main points when checking the test:
1.	compliance with the specified requirements
2.	use of specified technologies and libraries
3.	performance (under different given conditions)
4.	decomposition of code entities
5.	writing unit-tests (jest is preferable)

## Will be a plus:
1.	Using design patterns

<img width="372" alt="image" src="https://github.com/rden82/web-worker/assets/28786149/464a20e4-a522-45cd-8992-af436b2122db">
