# SP Decrypt RID
Use this module to decrypt a RID for a hidden field on the submission of a webform.
You need to add two variables (via Drush or in settings.php)

$conf['sp_decrypt_rid_forms'][1] = 4;  // set as key: form_id value: target_field
$conf['sp_decrypt_rid_key'] = 'abcd'; // Needs to be the same as on the encrypting end.

The RID is passed via an url-parameter (?rid=....) 
as a base64 encoded MCRYPT_RIJNDAEL_256 encrypted string.
