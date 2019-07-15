<h1>Add multiple contacts to sms blacklist</h1>
<p>Add multiple contacts to the user’s blacklist./p>
<blockquote>Remember to provide the authentication HTTP headers as described in the Authenticate using a session key and the Authenticate using a user token sections.</blockquote>
<blockquote>All the query string parameters in URL must be UTF-8 URL Encoded.</blockquote>
<hr>
<h2>HTTP Headers</h2>
<pre><code>user_key / Session_key</code></pre>
<h2>HTTP Method</h2>
<pre><code>POST</code></pre>
<h2>HTTP Request</h2>
<pre><code>https://app.gateway.smsend.it/API/v1.0/REST/contact/add_to_blacklist_batch</code></pre>
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
									<td>-</td>
									<td>List(String)</td>
									<td>Array of contact ids</td>
									<td>Yes</td>
									<td>"</td>
								</tr>
								</tbody></table>
								<blockquote>If one or more contact ids aren’t found, no contacts will be put in blacklist, and the response will have http status 400</blockquote>
<h2>Returns</h2>
<table class="table table-striped table-hover">
							<tbody><tr>
							  <th>Code</th>
							  <th>Description</th>
							</tr>
							<tr>
								<td>200</td>
								<td>Number of contacts correctly put in blacklist</td>
							</tr>
							<tr>
								<td>400</td>
								<td>Some of the contactsId specified were wrong</td>
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