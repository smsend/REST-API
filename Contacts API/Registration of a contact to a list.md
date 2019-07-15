<h1>Registration of a contact to a list</h1>
<p>Creates a new contact entry and adds it onto the specified campaign.</p>
<blockquote>Remember to provide the authentication HTTP headers as described in the Authenticate using a session key and the Authenticate using a user token sections.</blockquote>
<blockquote>All the query string parameters in URL must be UTF-8 URL Encoded.</blockquote>
<hr>
<h2>HTTP Headers</h2>
<pre><code>user_key / Session_key</code></pre>
<h2>HTTP Method</h2>
<pre><code>POST</code></pre>
<h2>HTTP Request</h2>
<pre><code>https://app.gateway.smsend.it/API/v1.0/REST/list/{campaign_id}/contact?SendOptIn={value}</code></pre>
<h2>Parameters</h2>
<table>
							<tbody><tr>
								<th>Parameter</th>
								<th>Type</th>
								<th>Description</th>
								<th>Required</th>
								<th>Default</th>
							</tr>
							<tr>
							  <td>campaign_id</td>
							  <td>Int</td>
							  <td>The campaign in which the contact will be added</td>
							  <td>Yes</td>
							  <td>-</td>
							</tr>
							<tr>
							  <td>SendOptIn</td>
							  <td>String, “true” or “false”</td>
							  <td>Send an Opt-In email to the contact’s email</td>
							  <td>No</td>
							  <td>“false”</td>
							</tr>
						</tbody></table>
<h2>Body Fields</h2>
<table>
							<tbody><tr>
								<th>Parameter</th>
								<th>Type</th>
								<th>Description</th>
								<th>Required</th>
								<th>Default</th>
							</tr>
							<tr>
							  <td>email</td>
							  <td>String</td>
							  <td>The email of the contact</td>
							  <td>Yes</td>
							  <td>-</td>
							</tr>
							<tr>
							  <td>phoneNumber</td>
							  <td>String</td>
							  <td>The phone number of the contact</td>
							  <td>No</td>
							  <td>“”</td>
							</tr>
							<tr>
							  <td>name</td>
							  <td>String</td>
							  <td>The first name of the contact</td>
							  <td>No</td>
							  <td>“”</td>
							</tr>
							<tr>
							  <td>surname</td>
							  <td>String</td>
							  <td>The last name of the contact</td>
							  <td>No</td>
							  <td>“”</td>
							</tr>
							<tr>
							  <td>gender</td>
							  <td>String</td>
							  <td>The gender of the contact</td>
							  <td>No</td>
							  <td>“”</td>
							</tr>
							<tr>
							  <td>fax</td>
							  <td>String</td>
							  <td>The Fax number of the contact</td>
							  <td>No</td>
							  <td>“”</td>
							</tr>
							<tr>
							  <td>address</td>
							  <td>String</td>
							  <td>The address of the contact</td>
							  <td>No</td>
							  <td>“”</td>
							</tr>
							<tr>
							  <td>city</td>
							  <td>String</td>
							  <td>The city of the contact</td>
							  <td>No</td>
							  <td>“”</td>
							</tr>
							<tr>
							  <td>province</td>
							  <td>String</td>
							  <td>The province of the contact</td>
							  <td>No</td>
							  <td>“”</td>
							</tr>
							<tr>
							  <td>birthdate</td>
							  <td>String [ddMMyy, yyyyMMdd, ddMMyyHHmm, yyyyMMddHHmmss, yyyy-MM-dd HH:mm, yyyy-MM-dd HH:mm.0]</td>
							  <td>The birth date of the contact</td>
							  <td>No</td>
							  <td>“”</td>
							</tr>
							<tr>
							  <td>zip</td>
							  <td>String</td>
							  <td>The ZIP code of the contact</td>
							  <td>No</td>
							  <td>“”</td>
							</tr>
							<tr>
							  <td>groupIds</td>
							  <td>List(String)</td>
							  <td>The groups (Ids) in which the contact will be added</td>
							  <td>No</td>
							  <td>[]</td>
							</tr>
						</tbody></table>
<h2>Returns</h2>
<table>
							<tbody><tr>
							  <th>Code</th>
							  <th>Description</th>
							</tr>
							<tr>
							  <td>201</td>
							  <td>The contact has been added and the HTTP Location Header returns its URL.</td>
							</tr>
							<tr>
							  <td>400</td>
							  <td>Campaign not active or not found, no email provided, group not owned or a generic error. Details are in the body</td>
							</tr>
							<tr>
							  <td>401</td>
							  <td><strong>[Unauthorized]</strong> User_key, Token or Session_key are invalid or not provided</td>
							</tr>
							<tr>
							  <td>404</td>
							  <td><strong>[Not found]</strong> The User_key was not found</td>
							</tr>
						</tbody></table>