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

## Get in touch ##
If you need further assistance, please contact lf@netnode.ch

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

## Event Entity ##

### Properties ###
<table>
<tr>
<td>contact_id</td>
<td>Contact id</td>
</tr>
<tr>
<td>event_type</td>
<td>Event type (pageview, lifecycle_stage_changed, submission, note)</td>
</tr>
<tr>
<td>title</td>
<td>The "title" of the event.</td>
</tr>
</table>


<table>
<tr>
<th colspan="3">Contact API Call</th>
<tr>
<td>GET</td>
<td>/api/v1/contact</td>
<td>Query contacts</td>
</tr>
<tr>
<td>POST</td>
<td>/api/v1/event</td>
<td>Create a new event. The contact_id always need to be set.</td>
</tr>
</table>


