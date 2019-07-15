<h1>Add a contacts group to a list of distribution</h1>
<p>Add all contacts of the given group to the given list of distribution.</p>
<p>Emails can be only sent to contacts that belong to a distribution list.</p>
<blockquote>Remember to provide the authentication HTTP headers as described in the Authenticate using a session key and the Authenticate using a user token sections.</blockquote>
<blockquote>All the query string parameters in URL must be UTF-8 URL Encoded.</blockquote>
<hr>
<h2>HTTP Headers</h2>
<pre><code>user_key / Session_key</code></pre>
<h2>HTTP Method</h2>
<pre><code>POST</code></pre>
<h2>HTTP Request</h2>
<pre><code>https://app.gateway.smsend.it/API/v1.0/REST/list/{list_id}/group/{group_id}?sendoptin={send}</code></pre>
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
								  <td>list_id</td>
								  <td>Int</td>
								  <td>The list ID</td>
								  <td>Yes</td>
								  <td>-</td>
								</tr>
								<tr>
								  <td>group_id</td>
								  <td>String</td>
								  <td>The group ID</td>
								  <td>Yes</td>
								  <td>-</td>
								</tr>
								<tr>
								  <td>sendoptin</td>
								  <td>Bool</td>
								  <td>Send the Opt-in email to the group’s contacts</td>
								  <td>No</td>
								  <td>false</td>
								</tr>
						</tbody></table>
<h2>Returns</h2>
<table>
							<tbody><tr>
								<th>Code</th>
								<th>Description</th>
							</tr>
							<tr>
							  <td>200</td>
							  <td>The group has been added to the list</td>
							</tr>
							<tr>
							  <td>400</td>
							  <td>Other errors, details are in the body</td>
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