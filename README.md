# openinbound-api

## Usage ##
<pre>$oi = new OI('YOUR_TRACKING_ID', 'YOUR_API_KEY');</pre>

## Examples ##
## Update an existing contact ##
<pre>
    $data['email'] = 'email'
    $data['first_name'] = 'Joe';
    $data['last_name'] = 'Long';
    $data['company_name'] = 'Company LCC';
    $oi = new OI('YOUR_TRACKING_ID', 'YOUR_API_KEY');
    $oi->updateContact($_COOKIE['_oi_contact_id'], $data);
</pre>

Note: The $$_COOKIE['_oi_contact_id'] will be automatically set by the OpenInbound tracking script.

## Contact ##
If you need further assistance, please contact lf@netnode.ch
