# soft-redirect-geobytes
Simple snippet to redirect the user on page load based on detected Country

## Usage
- Edit `redirect_to` and `if_country_is` to your desired values case-insensitive
- Upload to your hosting provider
- Profit

## Quick-view
```javascript
<html>
	<head>
		<!-- Don't forget to fill this -->
	</head>
	<body>
		<!-- Insert normal content here -->
		<script async defer SameSite="none" src="http://gd.geobytes.com/gd?after=-1&variables=GeobytesCountry"></script>
		<script>
      			//Edit these two lines below
			const redirect_to = "https://google.com";
			const if_country_is = "Spain";

			document.onreadystatechange = function () {
			    if (document.readyState == "interactive") {
			        if((window.sGeobytesCountry ? window.sGeobytesCountry : '').toLowerCase() === if_country_is.toLowerCase()) {
			        	//The country is as defined
			        	//window.location.href = redirect_to;
			        } else {
			        	//The country is not as defined
			        }
			    }
			}
		</script>
	</body>
</html> 
```
