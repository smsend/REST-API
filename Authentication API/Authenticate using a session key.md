<h1>Authenticate using a session key</h1>
<p>The login with session key API lets you authenticate by using your username and password, and returns a token to be used for authenticating the next API calls. The following HTTP headers should be provided after the login:</p>
<code>user_key:{USER_KEY}</code> <code>Session_key:{SESSION_KEY}</code>
<p>Where <code>{USER_KEY}</code> and <code>{SESSION_KEY}</code> are the values returned by the login API.</p>
<p><code>{USER_KEY}</code> and <code>{SESSION_KEY}</code> placeholders can be found in all code examples.</p>
<p>When actually running the example, the correct values must be used instead.</p>
<p>The returned session key expires when no API calls are performed for 5 minutes)</p>
<h2>HTTP Method</h2>
<kbd>GET</kbd>
<h2>HTTP Request</h2>
<kbd>https://app.gateway.smsend.it/API/v1.0/REST/login?username={USERNAME}&password={PASSWORD}</kbd>
<h2>Parameters</h2>
<table>
  <tbody>
    <tr>
      <th>Parameter</th>
      <th>Type</th>
      <th>Description</th>
      <th>Required</th>
      <th>Default</th>
    </tr>
    <tr>
      <td>username</td>
      <td>String</td>
      <td>Your account’s username</td>
      <td>Yes</td>
      <td>-</td>
    </tr>
    <tr>
      <td>password</td>
      <td>String</td>
      <td>Your account’s password</td>
      <td>Yes</td>
      <td>-</td>
    </tr>
  </tbody>
</table>
<h2>Returns</h2>
<table>
  <tbody>
    <tr>
      <th>Code</th>
      <th>Description</th>
    </tr>
    <tr>
      <td>200</td>
      <td>The user_key and the session_key</td>
    </tr>
    <tr>
      <td>404</td>
      <td><strong>[Not found]</strong> Credentials are incorrect</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Other errors, details are in the body</td>
    </tr>
  </tbody>
</table>
<h2>Code example</h2>
<pre><code># Session Key example
curl -XGET 'http://app.gateway.smsend.it/API/v1.0/REST/login?username={username}&password={password}' -H 'Content-Type: application/json'</code></pre>
<pre><code># Access token example
curl -XGET 'http://app.gateway.smsend.it/API/v1.0/REST/login?username={username}&password={password}' -H 'Content-Type: application/json'</code></pre>
