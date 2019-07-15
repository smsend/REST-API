<h1>Retrieve list of phone numbers in blacklist</h1>
<p>Retrieve the paginated list of Phone numbers in SMS Blacklist</p>
<blockquote>Remember to provide the authentication HTTP headers as described in the Authenticate using a session key and the Authenticate using a user token sections.</blockquote>
<blockquote>All the query string parameters in URL must be UTF-8 URL Encoded.</blockquote>
<hr>
<h2>HTTP Headers</h2>
<pre><code>user_key / Session_key</code></pre>
<h2>HTTP Method</h2>
<pre><code>GET</code></pre>
<h2>HTTP Request</h2>
<pre><code>https://app.gateway.smsend.it/API/v1.0/REST/blacklist/sms</code></pre>
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
								<td>from</td>
								<td>Date(yyyy-MM-dd HH:mm:ss)</td>
								<td>Return results from the given date</td>
								<td>No</td>
								<td>-</td>
							</tr>
							<tr>
								<td>to</td>
								<td>Date(yyyy-MM-dd HH:mm:ss)</td>
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
								<td>number</td>
								<td>String</td>
								<td>Return results that contains this phone number or part of it.</td>
								<td>No</td>
								<td>-</td>
							</tr>
							<tr>
								<td>origins</td>
								<td>String</td>
								<td>List of origins(API, WEB, STOPSMS) separated by ‘,’ used for filter the results</td>
								<td>No</td>
								<td>-</td>
							</tr>
							<tr>
								<td>pageNumber</td>
								<td>String</td>
								<td>Return the given results page</td>
								<td>No</td>
								<td>-</td>
							</tr>
							<tr>
								<td>pageSize</td>
								<td>String</td>
								<td>The number of results in a page</td>
								<td>No</td>
								<td>-</td>
							</tr>
						</tbody></table>
						<blockquote>If one or more phone numbers are badly formatted, no numbers will be put in blacklist, and the response will have http status 400</blockquote>
<h2>Returns</h2>
<table>
							<tbody><tr>
								<th>Code</th>
								<th>Description</th>
							</tr>
							<tr>
								<td>200</td>
								<td>A paginated list of phone number in blacklist.</td>
							</tr>
							<tr>
								<td>400</td>
								<td>Some of the parameters specified were badly formatted</td>
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