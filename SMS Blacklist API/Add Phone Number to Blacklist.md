<h1>Add Phone Number to Blacklist</h1>
<p>Add Phone Number to SMS Blacklist The Phone number will no longer receive an SMS from the user requesting the addition to the blacklist.</p>
<blockquote>Remember to provide the authentication HTTP headers as described in the Authenticate using a session key and the Authenticate using a user token sections.</blockquote>
<blockquote>All the query string parameters in URL must be UTF-8 URL Encoded.</blockquote>
<hr>
<h2>HTTP Headers</h2>
<pre><code>user_key / Session_key</code></pre>
<h2>HTTP Method</h2>
<pre><code>POST</code></pre>
<h2>HTTP Request</h2>
<pre><code>https://app.gateway.smsend.it/API/v1.0/REST/blacklist/sms</code></pre>
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
									<td>phoneNumber</td>
									<td>String</td>
									<td>The phone number of the user. The format must be +1111111111 or 001111111111</td>
									<td>Yes</td>
									<td>-</td>
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
									<td>The phone number is succesfully added.</td>
								</tr>
								<tr>
									<td>400</td>
									<td><strong>[Bad request]</strong> Invalid recipient.</td>
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