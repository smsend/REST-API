<a href="https://www.smsend.it/rest-api/" title="smSend developer guide"><img src="https://www.smsend.it/img/visual/smsend-developers.jpg" alt="smSend developer guide" title="smSend developer guide"></a>
<h1><b>smSend Rest-API</b></h1>
<a href="https://www.smsend.it/rest-api/" title="smSend developer guide">smsend.it</a>
<p>The API is divided into subsections, which are briefly described below.</p>
<p>For details about each section, please refer to the respective section and languages.</p>
<ol>
  <li>
    <p><b>Authentication:</b><br>
      This section describes how to authenticate requests to the smSend API. All API methods require authentication.</p>
    <ul>
      <li>
        Authentication  using a session key
      </li>
      <li>
        Authentication  using a user token
      </li>
    </ul>
  </li>
  <li>
    <p><b>User:</b><br>
      The following are utility functions regarding the Authenticated User (e.g. the user status, password reset, etc)</p>
    <ul>
      <li>
        Dashboard
      </li>
      <li>
        Verify session
      </li>
      <li>
        Reset password
      </li>
      <li>
        User status
      </li>
    </ul>
  </li>
  <li>
    <p><b>Contacts:</b><br>
      This part of the API is used to manage contacts. A contact can be used both in SMS and Email sending, provided that a phone number and/or an email address are given.</p>
    <ul>
      <li>
        Add a contact
      </li>
      <li>
        Add multiple contacts
      </li>
      <li>
        Get a contact
      </li>
      <li>
        Registration of a contact to a list
      </li>
      <li>
        List contact’s custom fields
      </li>
      <li>Add contact to sms blacklist</li>
      <li>Add multiple contacts to sms blacklist</li>
      <li>Add phone number to sms blacklist</li>
    </ul>
  </li>
  <li>
    <p><b>Contacts Groups:</b><br>
      This section describes how groups of contacts are created, updated and deleted. SMS messages and emails can be directly sent to groups of contacts.</p>
    <ul>
      <li>
        Create a contacts group
      </li>
      <li>
        Modify an existing contacts group
      </li>
      <li>
        Delete a contacts group
      </li>
      <li>
        List contacts groups
      </li>
      <li>
        Add a contact to a group
      </li>
      <li>
        Remove a contact from a group
      </li>
    </ul>
  </li>
  <li>
    <p><b>TPOA:</b><br>
      Here are described the methods to work with TPOA Aliases (Transmission Path Originating Address, i.e. the SMS Sender Alias). TPOA Aliases can be used only with some specific high quality SMS message types.</p>
    <ul>
      <li>
        Create a new alias
      </li>
      <li>
        Get all aliases
      </li>
      <li>
        Get a specific alias
      </li>
      <li>
        Remove an alias
      </li>
    </ul>
  </li>
  <li>
    <p><b>Sending SMS messages:</b><br>
      This is the part of the API that allows to send SMS messages, to single recipients, saved contacts or groups of contacts.</p>
    <ul>
      <li>
        Send an SMS message
      </li>
      <li>
        Send a parametric SMS message
      </li>
      <li>
        Send an SMS message to a group
      </li>
      <li>
        Get SMS message state
      </li>
      <li>
        Delete a scheduled message
      </li>
    </ul>
  </li>
  <li>
    <p><b>SMS messages history:</b><br>
      Used to retrieve the SMS messages sending history.</p>
    <ul>
      <li>
        Get sent SMS messages history
      </li>
    </ul>
  </li>
  <li>
    <p><b>SMS Blacklist / Stop SMS:</b><br>
      This section allow to insert and to retrieve the list of SMS blacklist / Stop SMS.</p>
    <ul>
      <li>
        Add Phone Number to Blacklist
      </li>
      <li>
        Add multiple numbers to sms blacklist
      </li>
      <li>
        Retrieve list of phone numbers in blacklist
      </li>
    </ul>
  </li>
  <li>
    <p><b>Receiving SMS messages:</b><br>
      The methods described in this section are used to retrieve the received SMS messages.</p>
    <ul>
      <li>
        Get new received messages
      </li>
      <li>
        Get the received SMS messages
      </li>
      <li>
        Get the received SMS messages after a specified message
      </li>
      <li>
        Get the MO received messages
      </li>
    </ul>
  </li>
  <li>
    <p><b>Landing pages API:</b><br>
      This is the part of the API that regards the Landing Pages service.</p>
    <ul>
      <li>
        List the published landing pages
      </li>
    </ul>
  </li>
  <li>
    <p><b>Email Campaign API:</b><br>
      This API exposes methods for creating and managing Email campaigns.</p>
    <ul>
      <li>
        Create a new list
      </li>
      <li>
        Modify a list
      </li>
      <li>
        Get list of campaigns by statuses
      </li>
      <li>
        Add a contacts group to a list of distribution
      </li>
      <li>
       Create a new email draft
      </li>
      <li>
        Create new issue using a specified template
      </li>
      <li>
        Send an issue to preloaded contacts
      </li>
    </ul>
  </li>
  <li>
    <p><b>Subaccounting:</b><br>
      If enabled as a superaccount, the user can create subaccounts that can be assigned to third-parties. Superaccounts may or may not share credits with their subaccounts.</p>
    <ul>
      <li>
        Get the list of subaccounts
      </li>
      <li>
        Create a subaccount
      </li>
      <li>
        Edit subaccount
      </li>
      <li>
        Change subaccount password
      </li>
      <li>
        Get subaccount
      </li>
      <li>
        Move credits from/to subaccount
      </li>
      <li>
        Get subaccount available credits
      </li>
      <li>
        Get a subaccount’s purchases
      </li>
      <li>
        Create a subaccount purchase
      </li>
      <li>
        Delete a subaccount’s purchase
      </li>
    </ul>
  </li>
  <li>
    <p><b>Two Factor authentication:</b><br>
      This API provides the Two Factor Authentication via SMS.</p>
    <ul>
      <li>
        Request a 2FA Pin
      </li>
      <li>
        Verify a 2FA Pin
      </li>
    </ul>
  </li>
</ol>
