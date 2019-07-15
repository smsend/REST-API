<h1>Create a new email draft</h1>
<p>Creates a new email draft. Every email draft must be associated to a distribution list.</p>
<blockquote>Remember to provide the authentication HTTP headers as described in the Authenticate using a session key and the Authenticate using a user token sections.</blockquote>
<blockquote>All the query string parameters in URL must be UTF-8 URL Encoded.</blockquote>
<hr>
<h2>HTTP Headers</h2>
<pre><code>user_key / Session_key</code></pre>
<h2>HTTP Method</h2>
<pre><code>POST</code></pre>
<h2>HTTP Request</h2>
<pre><code>https://app.gateway.smsend.it/API/v1.0/REST/list/{list_id}/issue</code></pre>
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
							  <td>list_id</td>
							  <td>Int</td>
							  <td>The list where to send the emails</td>
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
							  <td>title</td>
							  <td>String</td>
							  <td>The issue title</td>
							  <td>Yes</td>
							  <td>-</td>
							</tr>
							<tr>
							  <td>subject</td>
							  <td>String</td>
							  <td>The subject for the issue</td>
							  <td>Yes</td>
							  <td>-</td>
							</tr>
							<tr>
							  <td>share_social</td>
							  <td>Bool</td>
							  <td>Adds the social share buttons</td>
							  <td>Yes</td>
							  <td>-</td>
							</tr>
							<tr>
							  <td>web_analytics</td>
							  <td>String</td>
							  <td>The WebAnalytics tracing code</td>
							  <td>No</td>
							  <td>-</td>
							</tr>
							<tr>
							  <td>text_content</td>
							  <td>String</td>
							  <td>The Email text body</td>
							  <td>Yes</td>
							  <td>-</td>
							</tr>
							<tr>
							  <td>html_content</td>
							  <td>String</td>
							  <td>The Email HTML body</td>
							  <td>Yes</td>
							  <td>-</td>
							</tr>
							<tr>
							  <td>attachments</td>
							  <td>List(Attachment)</td>
							  <td>The list of attachments (can be empty)</td>
							  <td>Yes</td>
							  <td>-</td>
							</tr>
							<tr>
							  <td>Attachment.file_name</td>
							  <td>String</td>
							  <td>The file name of the attachment</td>
							  <td>Yes</td>
							  <td>-</td>
							</tr>
							<tr>
							  <td>Attachment.file_content_base64</td>
							  <td>String</td>
							  <td>The base64-encoded attachment</td>
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
								  <td>201</td>
								  <td>Issue created, the HTTP Location header points to the created issue</td>
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