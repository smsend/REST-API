<h1>Add a contact</h1>
<p>Add a contact to the user’s addressbook.</p>
<blockquote>Remember to provide the authentication HTTP headers as described in the Authenticate using a session key and the Authenticate using a user token sections.</blockquote>
<blockquote>All the query string parameters in URL must be UTF-8 URL Encoded.</blockquote>
<hr>
<h2>HTTP Headers</h2>
<pre><code>user_key / Session_key</code></pre>
<h2>HTTP Method</h2>
<pre><code>POST</code></pre>
<h2>HTTP Request</h2>
<pre><code>https://app.gateway.smsend.it/API/v1.0/REST/contact</code></pre>
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
									<td>email</td>
									<td>String (A valid email)</td>
									<td>The email of the contact</td>
									<td>Yes</td>
									<td>-</td>
								</tr>
								<tr>
									<td>phoneNumber</td>
									<td>String (A non empty string)</td>
									<td>The phone number of the contact</td>
									<td>Yes</td>
									<td>“”</td>
								</tr>
								<tr>
									<td>name</td>
									<td>String (max 40 chars)</td>
									<td>The first name of the contact</td>
									<td>No</td>
									<td>“”</td>
								</tr>
								<tr>
									<td>surname</td>
									<td>String (max 40 chars)</td>
									<td>The last name of the contact</td>
									<td>No</td>
									<td>“”</td>
								</tr>
								<tr>
									<td>gender</td>
									<td>String (“m” or “f”)</td>
									<td>The gender of the contact</td>
									<td>No</td>
									<td>“”</td>
								</tr>
								<tr>
									<td>fax</td>
									<td>String (max 32 chars)</td>
									<td>The Fax number of the contact</td>
									<td>No</td>
									<td>“”</td>
								</tr>
								<tr>
									<td>address</td>
									<td>String (max 256 chars)</td>
									<td>The address of the contact</td>
									<td>No</td>
									<td>“”</td>
								</tr>
								<tr>
									<td>city</td>
									<td>String (max 32 chars)</td>
									<td>The city of the contact</td>
									<td>No</td>
									<td>“”</td>
								</tr>
								<tr>
									<td>province</td>
									<td>String (max 32 chars)</td>
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
									<td>promotiondate</td>
									<td>String [ddMMyy, yyyyMMdd, ddMMyyHHmm, yyyyMMddHHmmss, yyyy-MM-dd HH:mm, yyyy-MM-dd HH:mm.0]</td>
									<td>An additional date field</td>
									<td>No</td>
									<td>“”</td>
								</tr>
								<tr>
									<td>rememberdate</td>
									<td>String [ddMMyy, yyyyMMdd, ddMMyyHHmm, yyyyMMddHHmmss, yyyy-MM-dd HH:mm, yyyy-MM-dd HH:mm.0]</td>
									<td>An additional date field</td>
									<td>No</td>
									<td>“”</td>
								</tr>
								<tr>
									<td>zip</td>
									<td>String (max 16 chars)</td>
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
								<tr>
									<td>custom1</td>
									<td>String</td>
									<td>Custom field 1</td>
									<td>No</td>
									<td>“”</td>
								</tr>
								<tr>
									<td>custom2</td>
									<td>String</td>
									<td>Custom field 2</td>
									<td>No</td>
									<td>“”</td>
								</tr>
								<tr>
									<td>custom3</td>
									<td>String</td>
									<td>Custom field 3</td>
									<td>No</td>
									<td>“”</td>
								</tr>
								<tr>
									<td>custom4</td>
									<td>String</td>
									<td>Custom field 4</td>
									<td>No</td>
									<td>“”</td>
								</tr>
								<tr>
									<td>custom5</td>
									<td>String</td>
									<td>Custom field 5</td>
									<td>No</td>
									<td>“”</td>
								</tr>
								<tr>
									<td>custom6</td>
									<td>String</td>
									<td>Custom field 6</td>
									<td>No</td>
									<td>“”</td>
								</tr>
								<tr>
									<td>custom7</td>
									<td>String</td>
									<td>Custom field 7</td>
									<td>No</td>
									<td>“”</td>
								</tr>
								<tr>
									<td>custom8</td>
									<td>String</td>
									<td>Custom field 8</td>
									<td>No</td>
									<td>“”</td>
								</tr>
								<tr>
									<td>custom9</td>
									<td>String</td>
									<td>Custom field 9</td>
									<td>No</td>
									<td>“”</td>
								</tr>
								<tr>
									<td>custom10</td>
									<td>String</td>
									<td>Custom field 10</td>
									<td>No</td>
									<td>“”</td>
								</tr>	
							</tbody></table>
                            <blockquote>At least one between the `email` and the `phoneNumber` fields has to be provided</blockquote>
<h2>Returns</h2>
<table>
								<tbody><tr>
									<th>Code</th>
									<th>Description</th>
								</tr>
								<tr>
								  <td>201</td>
								  <td>Empty string, and the HTTP Location header containing the path of the newly created contact</td>
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