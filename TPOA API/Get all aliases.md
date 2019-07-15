<h1>Get all aliases</h1>
<p>Returns a paginated list of the user’s TPOA aliases.</p>
<blockquote>Remember to provide the authentication HTTP headers as described in the Authenticate using a session key and the Authenticate using a user token sections.</blockquote>
<blockquote>All the query string parameters in URL must be UTF-8 URL Encoded.</blockquote>
<hr>
<h2>HTTP Headers</h2>
<pre><code>user_key / Session_key</code></pre>
<h2>HTTP Method</h2>
<pre><code>GET</code></pre>
<h2>HTTP Request</h2>
<pre><code>https://app.gateway.smsend.it/API/v1.0/REST/alias?pageNumber={page}&pageSize={size}&hide-not-approved={value}</code></pre>
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
								<tr>
								  <td>hide-not-approved</td>
								  <td>Bool</td>
								  <td>Show or hide not-yet-approved aliases</td>
								  <td>No</td>
								  <td>false</td>
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
							  <td>The paginated list of the user’s TPOA aliases</td>
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
			    	<p>The <pre><code>alias-state</code></pre> attribute in the returned objects represents the status of the TPOA confirmation process. It can be one of the following:</p>
					<table>
							<tbody><tr>
								<th>alias-state</th>
								<th>Description</th>
							</tr>
							<tr>
							  <td>0</td>
							  <td>Unconfirmed</td>
							</tr>
							<tr>
							  <td>1</td>
							  <td>Confirmed by smSend</td>
							</tr>
							<tr>
							  <td>2</td>
							  <td>Confirmed by AGCOM</td>
							</tr>
							<tr>
							  <td>3</td>
							  <td>Blocked by smSend</td>
							</tr>
							<tr>
							  <td>4</td>
							  <td>Blocked by AGCOM</td>
							</tr>
							<tr>
							  <td>9</td>
							  <td>The Alias has been pre-confirmed by smSend</td>
							</tr>
						</tbody></table>