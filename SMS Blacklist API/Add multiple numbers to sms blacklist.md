<h1>Add multiple numbers to sms blacklist</h1>
<p>Add multiple numbers to the user’s blacklist.</p>
<blockquote>Remember to provide the authentication HTTP headers as described in the Authenticate using a session key and the Authenticate using a user token sections.</blockquote>
<blockquote>All the query string parameters in URL must be UTF-8 URL Encoded.</blockquote>
<hr>
<h2>HTTP Headers</h2>
<pre><code>user_key / Session_key</code></pre>
<h2>HTTP Method</h2>
<pre><code>POST</code></pre>
<h2>HTTP Request</h2>
<pre><code>https://app.gateway.smsend.it/API/v1.0/REST/blacklist/smsbatch</code></pre>
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
								<td>—</td>
								<td>List(String)</td>
								<td>Array of phone numbers</td>
								<td>Yes</td>
								<td>“”</td>
							</tr>
						</tbody></table>
						<blockquote>If one or more phone numbers are badly formatted, no numbers will be put in blacklist, and the response will have http status 400</blockquote>
<h2>Returns</h2>
<table>
							<tbody><tr>
								<td>200</td>
								<td>Number of phone numbers correctly put in blacklist</td>
							</tr>
							<tr>
								<td>400</td>
								<td>Some of the phone numbers specified were badly formatted</td>
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