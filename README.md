alertjs.show({
	type: 'prompt',
	title: 'Please enter your name to continue',
	text: 'Enter your name here:',
	from: 'right', //slide from left
	success: function( val ) {
		//user clicked OK button
		//input box value will be available here
		var value = 'Your name is ' + val;
		if( val === '' ) {
			value = 'You didn\'t type anything!';
		}
		alertjs.show({
			title: 'Alert.js',
			from: 'top',
			effect: 'ease-in-bounce',
			text: value
		});
	},
	cancelled: function() {
		//user clicked cancel button
	},
	complete: function( status, val ) {
		console.log(status, val);
	}
});
