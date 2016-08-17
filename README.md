Link: www.louisianarescue.com

	/api/rescue/ [GET]
		Returns Array of all Objects.
	EXAMPLE:
		{
		  "request": [
			{
			  "updated_on": "2016-08-17T21:23:51.218Z",
			  "name":"a",
			  "people":"",
			  "level":"Unknown",
			  "pet":"No Pets",
			  "number":"",
			  "contact":"b",
			  "address":" 374 Mission Dr, Simmesport, LA 71369",
			  "info":"",
			  "status": "Pending",
			  "pin": "59399",
			}
		  ]
		}
	
	/api/rescue/map [GET]
		Returns Array of Lat, Lng, ID for Google Maps
	EXAMPLE:
		[
		  {
			"id": "57b4d5e7e890f0dfbf91e3d2",
			"latitude": 39.9129412,
			"longitude": -104.7956055
		  }
		]
	
	/api/rescue/help [POST]
	EXAMPLE BODY:
		{
		  "name": "Real Test 8",
		  "people": "",
		  "level": "Unknown",
		  "pet": "No Pets",
		  "number": "",
		  "contact": "",
		  "email": "",
		  "address": " 372 Mission Dr, Simmesport, LA 71369",
		  "info": ""
		}
	Error Return:
		{
		  "success": false,
		  "message": "Error Message Here"
		}
	Working Return:
		{
		  "success": true,
		  "message": "Just a Statement Saying it was Added."
		}
	
	/api/rescue/check/:pin [GET]
		Checking the Status of a Post, via its Pin. This is for tropo or other Services that want to check the Status of a Request.
	Error Return:
		{
		  "success": false,
		  "message": "Error Message Here"
		}
	Working Return:
		{
		  "success": true,
		  "message": "Just a Statement Saying it was Added.",
		  "data": {
			"status": "Pending",
			"rescued_on": "Date",
			"updated_on": "Date"
		  }
		}
	
