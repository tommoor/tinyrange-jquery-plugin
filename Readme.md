# Jquery Tiny Range

Tiny Range is a small jquery slider plugin that augments the html5 range element to make it styleable and adds additional options such as multiple handles.

Why bother when jQuery UI exists? jQuery UI is awesome, but the dependencies for the slider alone is ~22Kb. Tiny range is much smaller and nimbler at only 2Kb.


## Documentation

### simple usage

Just call the range() function on any range input in jquery to the element with a tiny range instance. Attributes on the input such as 'min', 'max' and 'step' will be used by the plugin.


__Example__

        $('input[type=range]').range();


### options

The plugin currently accepts three options

* range (Boolean) - Whether to allow the user to select a range between two values.
* change (Function) - An event fired when the slider is updated by the user (this can fire many times)
* blur (Function) - An event fired when the slider loses focus
* snap (Integer) - Forces range slider to snap at divisions (can also be set using the input 'step' attribute)

__Example 1__

    $('input[type=range]').range({
			range: true
		});


__Example 2__

    $('input[type=range]').range({
			change: function(values){
				// do something with new value(s)
				alert(values);
			},
			blur: function(values){
				// do something with new value(s)
				alert(values);
			}
		});


### destroy

In the event that you need to remove the plugin you can do so cleanly by passing 'destroy' as the first argument to the plugin


__Example__

     $('input[type=range]').range('destroy');


