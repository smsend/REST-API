<h1>Add multiple contacts</h1>
<p>Add multiple contacts to the user’s addressbook.</p>
<blockquote>Remember to provide the authentication HTTP headers as described in the Authenticate using a session key and the Authenticate using a user token sections.</blockquote>
<blockquote>All the query string parameters in URL must be UTF-8 URL Encoded.</blockquote>
<hr>
<h2>HTTP Headers</h2>
<pre><code>user_key / Session_key</code></pre>
<h2>HTTP Method</h2>
<pre><code>POST</code></pre>
<h2>HTTP Request</h2>
<pre><code>https://app.gateway.smsend.it/API/v1.0/REST/contact</code></pre>
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
									<td>contacts</td>
									<td>Json array of Contacts</td>
									<td>Array of Json object, formatted as <a href="https://www.smsend.it/rest-api/sms-contacts-api.aspx#ca1">ADD a contact</a></td>
									<td>Yes</td>
									<td>“”</td>
								</tr>
								<tr>
									<td>updateExistingContact</td>
									<td>boolean</td>
									<td>True to update existing contacts in case of clash, false to drop and insert them</td>
									<td>No</td>
									<td>false</td>
								</tr>
								<tr>
									<td>keepExistingGroupsAndCampaigns</td>
									<td>boolean</td>
									<td>True to keep all old contact groups associations and campaigns subscription</td>
									<td>No</td>
									<td>false</td>
								</tr>	
							</tbody></table>
                            <blockquote>At least one between the `email` and the `phoneNumber` fields has to be provided</blockquote>
							<blockquote>If one or more contacts are badly formatted, no contacts will be saved, and the response will have http status 400</blockquote>
<h2>Returns</h2>
<table>
								<tbody><tr>
									<th>Code</th>
									<th>Description</th>
								</tr>
								<tr>
									<td>200</td>
									<td>Number of contacts correctly created</td>
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