<h1>Request a 2FA Pin</h1>
<p>Request a Two Factor Authentication via text message. This method generates a pin and sends it via text message to the user.</p>
<blockquote>Remember to provide the authentication HTTP headers as described in the Authenticate using a session key and the Authenticate using a user tokeny sections.</blockquote>
<blockquote>All the query string parameters in URL must be UTF-8 URL Encoded.</blockquote>
<hr>
<h2>HTTP Headers</h2>
<pre><code>user_key / Session_key</code></pre>
<h2>HTTP Method</h2>
<pre><code>POST</code></pre>
<h2>HTTP Request</h2>
<pre><code>https://app.gateway.smsend.it/API/v1.0/REST/2fa/request</code></pre>
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
							<td>recipient</td>
							<td>String</td>
							<td>The phone number of the user. The format must be +1111111111 or 001111111111</td>
							<td>Yes</td>
							<td>-</td>
						</tr>
						<tr>
							<td>senderName</td>
							<td>String</td>
							<td>The sender name or number for the text message</td>
							<td>No</td>
							<td>Preferred Sender Name</td>
						</tr>
						<tr>
							<td>expiry</td>
							<td>Integer</td>
							<td>The expiration time of the PIN, in minutes</td>
							<td>No</td>
							<td>60</td>
						</tr>
						<tr>
							<td>messageBody</td>
							<td>String</td>
							<td>The message body. <br>PIN position in the text can be specified using the %PIN% placeholder. <br>If the placeholder is not provided the pin will be added at the end of message body.</td>
							<td>No</td>
							<td>A default message body per language.</td>
						</tr>					
					</tbody></table>
<h2>Returns</h2>
<table>
								<tbody><tr>
									<td>Code</td>
									<td>Description</td>
								</tr>
								<tr>
									<td>200</td>
									<td>Pin has been successfully sent via text message.</td>
								</tr>
								<tr>
									<td>400</td>
									<td><strong>[Bad request]</strong> Invalid recipient, senderName, expiry, or sending errors like not enough credit.</td>
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