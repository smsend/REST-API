<h1>Get the received SMS messages after a specified message.</h1>
<p>Returns a list (limited to max. 100 entries) of SMS messages received after the given SMS message ID id_message, for the given SIM id_sim.</p>
<blockquote>Remember to provide the authentication HTTP headers as described in the Authenticate using a session key and the Authenticate using a user token sections.</blockquote>
<blockquote>All the query string parameters in URL must be UTF-8 URL Encoded.</blockquote>
<hr>
<h2>HTTP Headers</h2>
<pre><code>user_key / Session_key</code></pre>
<h2>HTTP Method</h2>
<pre><code>GET</code></pre>
<h2>HTTP Request</h2>
<pre><code>https://app.gateway.smsend.it/API/v1.0/REST/srsmshistory/{id_sim}/{id_message}?limit={limit}</code></pre>
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
							  <td>String (Phone number)</td>
							  <td>The phone number where you enabled the service of reception, in international format (+393471234567 or 00393471234567)</td>
							  <td>Yes</td>
							  <td>-</td>
							</tr>
							<tr>
							  <td>id_message</td>
							  <td>Int</td>
							  <td>The reference message ID</td>
							  <td>Yes</td>
							  <td>-</td>
							</tr>
							<tr>
							  <td>limit</td>
							  <td>Int (max. 100)</td>
							  <td>The max. number of entries in the returned list</td>
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
							  <td>201</td>
							  <td>The contact has been added and the HTTP Location Header returns its URL.</td>
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