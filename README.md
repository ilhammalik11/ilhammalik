IlhamActionColumn
=================
Yii2-admin integration  Action Column by User

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist ilhammalik/ilhammalik "*"
```

or add

```
"ilhammalik/ilhammalik": "*"
```

to the require section of your `composer.json` file.


Usage
-----

Once the extension is installed, simply use it in your code by  :

Add Code common\config\bootstrap.php

//add this
```
Yii::$container->set('yii\grid\ActionColumn', [
   'class' => 'common\components\ActionColumn',
   'visibleCallback' => function($name) {
       return \Yii::$app->user->can($name);
   },
]);
```
