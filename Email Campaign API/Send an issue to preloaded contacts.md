<h1>Send an issue to preloaded contacts</h1>
<p>Schedule an issue to be sent to a specified list of contacts Ids at a given time.</p>
<blockquote>Remember to provide the authentication HTTP headers as described in the Authenticate using a session key and the Authenticate using a user token sections.</blockquote>
<blockquote>All the query string parameters in URL must be UTF-8 URL Encoded.</blockquote>
<hr>
<h2>HTTP Headers</h2>
<pre><code>user_key / Session_key</code></pre>
<h2>HTTP Method</h2>
<pre><code>POST</code></pre>
<h2>HTTP Request</h2>
<pre><code>https://app.gateway.smsend.it/API/v1.0/REST/list/{campaignId}/issue/{idIssue}</code></pre>
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
								  <td>campaignId</td>
								  <td>Int</td>
								  <td>The campaign where to send the emails</td>
								  <td>Yes</td>
								  <td>-</td>
								</tr>
								<tr>
								  <td>idIssue</td>
								  <td>Int</td>
								  <td>The mailing to send</td>
								  <td>Yes</td>
								  <td>-</td>
								</tr>
						</tbody></table>
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
								  <td>contactIds</td>
								  <td>String[]</td>
								  <td>The list of contact Ids of the recipients</td>
								  <td>Yes</td>
								  <td>-</td>
								</tr>
								<tr>
								  <td>scheduleTime</td>
								  <td>String</td>
								  <td>When send the mailing in format yyyy-MM-dd hh:mm:ss</td>
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
							  <td>Successful request</td>
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
							<tr>
							  <td>500</td>
							  <td>The issue can’t be sent or the contacts Ids array is empty</td>
							</tr>
						</tbody></table>