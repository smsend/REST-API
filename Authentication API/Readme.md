<h1>Authentication API</h1>
<h2>Authentication methods</h2>
<p>The following are the two available methods to authenticate a user, given a username and a password (registration required):</p>
<ul>
<li>Using a temporary session key, which expires after a certain amount of time has passed with no performed API calls with that key.</li>
<li>Using a temporary session key, which expires after a certain amount of time has passed with no performed API calls with that key.</li>
</ul>
<p>In both cases, the returned user_key, as well as the session key or the token, are required to be provided in the HTTP request headers in order to perform any API call after the login.</p>