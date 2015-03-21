# Rational Meta Box Generator
Generates meta boxes for WordPress using fields passed via arrays.

## Installation
```php
require_once('rational-meta-box.class.php');
$rational_meta_box = new RationalMetaBox();

function rational_meta_box_class() {
	global $rational_meta_box;
	$rational_meta_box->add_box();
}
add_action( 'add_meta_boxes', 'rational_meta_box_class' );
```

## Usage
Meta box parameters are set by passing an array as the first parameter in the `add_box` method.

```php
$my_attributes = array(
	'id'			=> 'my-meta-box',
	'title'			=> 'My Meta Box',
);
$rational_meta_box->add_box( $my_attributes );
```
### All Meta Box Parameters
Essentially the same as [WordPress' add_meta_box() parameters](http://codex.wordpress.org/Function_Reference/add_meta_box).
* **id**: HTML id attribute of meta box element (default: 'rational-meta-box')
* **title**: Title of meta box (default: 'Rational Meta Box')
* **screen**: Location, or post type, of the meta box (default: 'post')
* **context**: Region where the meta box is displayed (default: 'advanced')
* **priority**: Priority of the meta box within it's region (default: 'default')

## Contributing
1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request

## Version
0.1

## History
* 0.1 - Initial upload

## Todo's
* Get list of available styles for inputs
* Meta box `callback_args`

## License

The MIT License (MIT)

Copyright (c) 2015 Jeremy Hixon

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
