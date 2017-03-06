# openinbound-api

## Usage ##
<pre>$oi = new OI('YOUR_TRACKING_ID', 'YOUR_API_KEY');</pre>

Note: You'll find your tracking id and API on the settings page on app.openinbound.com.

## Examples ##
## Update an existing contact ##
<pre>
    $data['email'] = 'email'
    $data['first_name'] = 'Joe';
    $data['last_name'] = 'Long';
    $data['company_name'] = 'Company LCC';
    $data['phone'] = '041 450 10 66';
    $oi = new OI('YOUR_TRACKING_ID', 'YOUR_API_KEY');
    $oi->updateContact($_COOKIE['_oi_contact_id'], $data);
</pre>

Note: The $_COOKIE['_oi_contact_id'] will be automatically set by the OpenInbound tracking script.

## Contact ##
If you need further assistance, please contact lf@netnode.ch

## API Reference ##

<table>
<tr>
<th colspan="3">Contact API Call</th>
<tr>
<td>GET</td>
<td>/api/v1/contact</td>
<td>Query contacts</td>
</tr>
<tr>
<td>GET</td>
<td>/api/v1/contact/{{id}}</td>
<td>Get single contact</td>
</tr>
</table>

