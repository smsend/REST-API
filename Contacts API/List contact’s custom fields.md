<h1>List contact’s custom fields</h1>
<p>Returns the list of user’s defined custom fields</p>
<blockquote>Remember to provide the authentication HTTP headers as described in the Authenticate using a session key and the Authenticate using a user token sections.</blockquote>
<blockquote>All the query string parameters in URL must be UTF-8 URL Encoded.</blockquote>
<hr>
<h2>HTTP Headers</h2>
<pre><code>user_key / Session_key</code></pre>
<h2>HTTP Method</h2>
<pre><code>GET</code></pre>
<h2>HTTP Request</h2>
<pre><code>https://api.smsend.it/API/v1.0/REST/contacts/fields</code></pre>
<h2>Returns</h2>
<table>
							<tbody><tr>
							  <th>Code</th>
							  <th>Description</th>
							</tr>
							<tr>
								<td>200</td>
								<td>Successful request</td>
							</tr>
							<tr>
								<td>400</td>
								<td>Other errors, details are in the body</td>
							</tr>
							<tr>
								<td>401</td>
								<td><strong>[Unauthorized]</strong> User_key, Token or Session_key are invalid or not provided</td>
							</tr>
						</tbody></table>