# openinbound-api

## Usage ##
<pre>$oi = new OI('YOUR_TRACKING_ID', 'YOUR_API_KEY');</pre>

Note: You'll find your tracking id and API on the settings page on app.openinbound.com.

## Examples ##
## Update an existing contact ##
```php
    $data['email'] = 'email'
    $data['first_name'] = 'Joe';
    $data['last_name'] = 'Long';
    $data['company_name'] = 'Company LCC';
    $data['phone'] = '041 450 10 66';
    $oi = new OI('YOUR_TRACKING_ID', 'YOUR_API_KEY');
    $oi->updateContact($_COOKIE['_oi_contact_id'], $data);
```
    
</pre>

## Log a custom event to the OpenInbound backend ##
```php
    $data['title'] = 'This title will be sent in the OpenInbound event list';
    $data['event_type'] = 'raw';
    $data['raw'] = 'Whatever data you want to send.';
    $oi = new OI('YOUR_TRACKING_ID', 'YOUR_API_KEY');
    $oi->addEvent($_COOKIE['_oi_contact_id'], $data);
```


Note: The $_COOKIE['_oi_contact_id'] will be automatically set by the OpenInbound tracking script.

## Get in touch ##
If you need further assistance, please contact lf@netnode.ch


<hr>
# API Reference ###

## Contact Entity ##

### Properties ###
<table>
<tr>
<td>email</td>
<td>Contacts email address</td>
</tr>
<tr>
<td>first_name</td>
<td>First name of contact</td>
</tr>
<tr>
<td>last_name</td>
<td>Last name of contact</td>
</tr>
<tr>
<td>company_name</td>
<td>Company name of contact</td>
</tr>
<tr>
<td>phone</td>
<td>Phone number of contact</td>
</tr>
</table>

## Event Entity ##

### Properties ###
<table>
<tr>
<td>contact_id</td>
<td>Contact id</td>
</tr>
<tr>
<td>event_type</td>
<td>Event type (pageview, lifecycle_stage_changed, submission, raw)</td>
</tr>
<tr>
<td>title</td>
<td>The "title" of the event.</td>
</tr>
<tr>
<td>raw</td>
<td>Any data you want to save.</td>
</tr>
</table>

