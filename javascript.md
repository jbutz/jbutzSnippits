Date Formatting
===============
I use the PHP format m/d/y a lot, but JavaScript doesn't make that easy. This function fixes that
```javascript
Date.prototype.getPHPString = function()
{
	var m = this.getMonth() + 1;
	if(m < 10) m = "0"+String(m);
	var day = this.getDate();
	if(day < 10) day = "0"+String(day);
	var y = String(this.getFullYear()).substring(2);
	return m+'/'+day+'/'+y;
};
```
