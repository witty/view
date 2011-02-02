## View Class

I like kohana's View, so I ported.

### Basic Usage

	require '/home/lzyy/projects/os/witty/modules/witty/witty.php';
	Witty::init();

	$config = array(
		'template_path' => __DIR__.'/template',
	);

	// 2th param is template name
	$view = Witty::factory('View', 'hello.php', $config);

	// $view->foo = 'bar';

	// $view->set(array(
	// 	'foo' => 'bar',
	// ));

	$view->bind('foo', $foo);
	$foo = 'bar';

	echo $view;
	//echo $view->render('hello.php');

