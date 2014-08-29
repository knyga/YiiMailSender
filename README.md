YiiMailSender
=============
```php
		'mailSender'=>array(
			'class'=>'ext.mailSender.MailSender',
			'viewPath'=>'application.views.mail',
			'templates'=>array(
				'password-reset-required'=>array('subject'=>'Password reset required'),
				'password-reset-requested'=>array('subject'=>'Password reset'),
				'password-reset'=>array('subject'=>'Password changed'),
				'password-setup-first-admin'=>array('subject'=>'Welcome to Shaman!'),
				'password-setup'=>array('subject'=>'Welcome to Shaman!'),
				'presentation-assigned'=>array('subject'=>'A new presentation is available on Shaman!'),
				'presentation-revoked'=>array('subject'=>'Presentation revoked'),
				'presentation-updated'=>array('subject'=>'Presentation update available!'),
				'handout-viewed'=>array('subject'=>'Handout viewed'),
			),
		),
```

```php
		$ms=Yii::app()->mailSender;
		$ms->setTemplate('password-setup-first-admin', array(
			'link' => $link,
			'user' => $this
			)
		);

		$ms->send($this->email);
```
