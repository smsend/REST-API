<h1>Delete a scheduled message</h1>
<p>Deletes the SMS delivery process of the given order_id.</p>
<blockquote>Remember to provide the authentication HTTP headers as described in the Authenticate using a session key and the Authenticate using a user token sections.</blockquote>
<blockquote>All the query string parameters in URL must be UTF-8 URL Encoded.</blockquote>
<hr>
<h2>HTTP Headers</h2>
<pre><code>user_key / Session_key</code></pre>
<h2>HTTP Method</h2>
<pre><code>DELETE</code></pre>
<h2>HTTP Request</h2>
<pre><code>https://app.gateway.smsend.it/API/v1.0/REST/sms/{order_id}</code></pre>
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
							  <td>order_id</td>
							  <td>String</td>
							  <td>The order ID</td>
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
							  <td>Scheduled Message sending</td>
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
							  <td><strong>[Not found]</strong> The given <kbd>order_id</kbd> was not found, or the message sending could not be removed (e.g. Message status is not “SCHEDULED”)</td>
							</tr>
						</tbody></table>