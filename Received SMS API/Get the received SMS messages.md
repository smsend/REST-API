<h1>Get the received SMS messages</h1>
<p>Get the paginated list of received SMS messages.</p>
<blockquote>Remember to provide the authentication HTTP headers as described in the Authenticate using a session key and the Authenticate using a user token sections.</blockquote>
<blockquote>All the query string parameters in URL must be UTF-8 URL Encoded.</blockquote>
<hr>
<h2>HTTP Headers</h2>
<pre><code>user_key / Session_key</code></pre>
<h2>HTTP Method</h2>
<pre><code>GET</code></pre>
<h2>HTTP Request</h2>
<p>For all SIMs use:</p>
<pre><code>https://app.gateway.smsend.it/API/v1.0/REST/srsmshistory?from={fromdate}&to={todate}&pageNumber={page}&pageSize={size}</code></pre>
<p>For one or more specific SIMs, use:</p>
<pre><code>https://app.gateway.smsend.it/API/v1.0/REST/srsmshistory/{id_sim}?from={fromdate}&to={todate}&pageNumber={page}&pageSize={size}</code></pre>
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
								<td>from</td>
								<td>Date(yyyyMMddHHmmss)</td>
								<td>Return results from the given date</td>
								<td>Yes</td>
								<td>-</td>
								</tr>
								<tr>
								<td>to</td>
								<td>Date(yyyyMMddHHmmss)</td>
								<td>Return results up to the given date</td>
								<td>No</td>
								<td>now</td>
								</tr>
								<tr>
								<td>timezone</td>
								<td>Timezone(IANA time zone)</td>
								<td>Optional timezone applied to <kbd class="pre">from</kbd> or <kbd class="pre">to</kbd> dates</td>
								<td>No</td>
								<td>-</td>
								</tr>
								<tr>
								<td>pageNumber</td>
								<td>Int</td>
								<td>Return the given results page</td>
								<td>No</td>
								<td>1</td>
								</tr>
								<tr>
								<td>pageSize</td>
								<td>Int</td>
								<td>The number of results in a page</td>
								<td>No</td>
								<td>10</td>
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
							  <td>The paginated list of received SMS messages.</td>
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