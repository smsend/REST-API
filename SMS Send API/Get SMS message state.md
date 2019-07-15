<h1>Get SMS message state</h1>
<p>Get informations on the SMS delivery status of the given order_id.</p>
<blockquote>Remember to provide the authentication HTTP headers as described in the Authenticate using a session key and the Authenticate using a user token sections.</blockquote>
<blockquote>All the query string parameters in URL must be UTF-8 URL Encoded.</blockquote>
<hr>
<h2>HTTP Headers</h2>
<pre><code>user_key / Session_key</code></pre>
<h2>HTTP Method</h2>
<pre><code>GET</code></pre>
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
							  <td>A Json object representing the status of the given SMS order.</td>
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
							  <td><strong>[Not found]</strong> The order_id was not found</td>
							</tr>
						</tbody></table>
						<h2>Possible returned statuses are:</h2>
						<table>
							<tbody><tr>
								<th>Status</th>
								<th>Value</th>
							</tr>
							<tr>
								<td>WAITING</td>
								<td>“WAITING”</td>
								</tr>
								<tr>
								<td>SENT_TO_SMSC</td>
								<td>“SENT”</td>
								</tr>
								<tr>
								<td>WAITING_DELIVERY</td>
								<td>“WAIT4DLVR”</td>
								</tr>
								<tr>
								<td>SENT</td>
								<td>“SENT”</td>
								</tr>
								<tr>
								<td>DELIVERY_RECEIVED</td>
								<td>“DLVRD”</td>
								</tr>
								<tr>
								<td>TOO_MANY_SMS_FROM_USER</td>
								<td>“TOOM4USER”</td>
								</tr>
								<tr>
								<td>TOO_MANY_SMS_FOR_NUMBER</td>
								<td>“TOOM4NUM”</td>
								</tr>
								<tr>
								<td>ERROR</td>
								<td>“ERROR”</td>
								</tr>
								<tr>
								<td>TIMEOUT</td>
								<td>“TIMEOUT”</td>
								</tr>
								<tr>
								<td>UNPARSABLE_RCPT</td>
								<td>“UNKNRCPT”</td>
								</tr>
								<tr>
								<td>UNKNOWN_PREFIX</td>
								<td>“UNKNPFX”</td>
								</tr>
								<tr>
								<td>SENT_IN_DEMO_MODE</td>
								<td>“DEMO”</td>
								</tr>
								<tr>
								<td>WAITING_DELAYED</td>
								<td>“SCHEDULED”</td>
								</tr>
								<tr>
								<td>INVALID_DESTINATION</td>
								<td>“INVALIDDST”</td>
								</tr>
								<tr>
								<td>NUMBER_BLACKLISTED</td>
								<td>“BLACKLISTED”</td>
								</tr>
								<tr>
								<td>NUMBER_USER_BLACKLISTED</td>
								<td>“BLACKLISTED”</td>
								</tr>
								<tr>
								<td>SMSC_REJECTED</td>
								<td>“KO”</td>
								</tr>
								<tr>
								<td>INVALID_CONTENTS</td>
								<td>“INVALIDCONTENTS”</td>
								</tr>
						</tbody></table>