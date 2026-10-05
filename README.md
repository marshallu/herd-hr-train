Herd HR Training
===

Registration form CAPTCHA
---

The frontend training registration form uses Google reCAPTCHA v2. Configure the
public site key and private secret key in the **HR Registration Settings** page
in WordPress. The settings page is restricted to administrators.

For automated deployments, the keys may also be supplied in `wp-config.php`:

```php
define( 'MU_HR_TRAINING_RECAPTCHA_SITE_KEY', 'your-site-key' );
define( 'MU_HR_TRAINING_RECAPTCHA_SECRET_KEY', 'your-secret-key' );
```

The secret key must never be exposed in frontend code or committed to the
repository. The registration is rejected unless Google successfully verifies
the CAPTCHA response before ACF saves the registration post.
