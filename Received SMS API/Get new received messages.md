<h1>Add Phone Number to Blacklist</h1>
<p>Returns the list of received messages on the given sim_id since the last call of this method, or the beginning of time if it’s the first call. The list is limited to max. 100 entries.</p>
<blockquote>This method requires activation by smSend. If you want to request the received SMS messages through this API, please contact us at helpdesk@smsend.it</blockquote>
<blockquote>Remember to provide the authentication HTTP headers as described in the Authenticate using a session key and the Authenticate using a user token sections.</blockquote>
<blockquote>All the query string parameters in URL must be UTF-8 URL Encoded.</blockquote>
<hr>
<h2>HTTP Headers</h2>
<pre><code>user_key / Session_key</code></pre>
<h2>HTTP Method</h2>
<pre><code>GET</code></pre>
<h2>HTTP Request</h2>
<p>For all SIMs use:</p>
<pre><code>https://app.gateway.smsend.it/API/v1.0/REST/newsrsmsmessage?limit={limit}</code></pre>
<p>For one or more specific SIMs, use:</p>
<pre><code>https://app.gateway.smsend.it/API/v1.0/REST/newsrsmsmessage/{id_sim}?limit={limit}</code></pre>
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
								  <td>id_sim</td>
								  <td>String(PhoneNumber)</td>
								  <td>The phone number where you enabled the service of reception, in international format (+393471234567 or 00393471234567). If no SIM is specified, returns the new messages for all enabled SIMs. It is possible to specify more numbers, separated by comma</td>
								  <td>No</td>
								  <td>All SIMs</td>
								</tr>
								<tr>
								  <td>limit</td>
								  <td>Int (max 100)</td>
								  <td>The max. number of entries returned</td>
								  <td>No</td>
								  <td>100</td>
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
								  <td>The list of received SMS messages since the last call of this method.</td>
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