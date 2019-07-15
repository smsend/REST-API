<h1>Get the MO received messages.</h1>
<p>This feature is available only for French customers!. Returns a list (limited to max. 100 entries) of MO messages received for the give type which could be STOP or CONTACT or OTHER; type is a mandatory parameter, the other are optional.</p>
<blockquote>Remember to provide the authentication HTTP headers as described in the Authenticate using a session key and the Authenticate using a user token sections.</blockquote>
<blockquote>All the query string parameters in URL must be UTF-8 URL Encoded.</blockquote>
<hr>
<h2>HTTP Headers</h2>
<pre><code>user_key / Session_key</code></pre>
<h2>HTTP Method</h2>
<pre><code>GET</code></pre>
<h2>HTTP Request</h2>
<pre><code>https://app.gateway.smsend.it/API/v1.0/REST/mosmshistory?type=TYPE&from=FROMDATE&to=TODATE&pageNumber=PAGE&pageSize=SIZE</code></pre>
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
								<td>type</td>
								<td>String (“STOP” or “CONTACT” or “OTHER”)</td>
								<td>Type of the MO and could be one of STOP, CONTACT or OTHER</td>
								<td>Yes</td>
								<td>-</td>
								</tr>
								<tr>
								<td>from</td>
								<td>Date(yyyyMMddHHmmss)</td>
								<td>Return results from the given date</td>
								<td>No</td>
								<td>-</td>
								</tr>
								<tr>
								<td>to</td>
								<td>Date(yyyyMMddHHmmss)</td>
								<td>Return results up to the given date</td>
								<td>No</td>
								<td>-</td>
								</tr>
								<tr>
								<td>timezone</td>
								<td>Timezone(IANA time zone)</td>
								<td>Optional timezone applied to <kbd>from</kbd> or <kbd>to</kbd> dates</td>
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
								<td>The list of received MO messages of type, with the specified time constraints (if any) and paging</td>
								</tr>
								<tr>
								<td>400</td>
								<td>Other errors, details are in the body</td>
								</tr>
								<tr>
								<td>401</td>
								<td><strong>[Unauthorized]</strong> User_key, Token or Session_key are invalid or not provided, ot if the user is not French</td>
								</tr>
								<tr>
								<td>404</td>
								<td><strong>[Not found]</strong> The User_key was not found</td>
								</tr>
						</tbody></table>