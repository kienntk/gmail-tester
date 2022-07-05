#  Retrieve Gmail:
## 1. Get credentials.json
- Follow [Create a client ID and client secret](https://developers.google.com/adwords/api/docs/guides/authentication#create_a_client_id_and_client_secret "Create a client ID and client secret") to create new project on Google API Console. Remember to select **Desktop App** for the **Application type**
- Go to **OAuth consent screen** menu in the left panel to configure application. Remember to select **External** user type. In the next step, consider the SCOPE of gmail, follow [this link to get the correct SCOPE](https://developers.google.com/identity/protocols/oauth2/scopes "link").
- Go to **Credentials** menu, Create new Credentials and choose OAuth Client ID option. After finish, click Download button to download Client ID json file. 
- Rename to **credentials.json**. Copy to **plugins** folder Open the file, modify the Redirect URI value if it is not the same as [this image](https://camo.githubusercontent.com/0495d8fe1550b2710d785b853f6dcb228301ddf08683de067eaf8186dc3c45ff/68747470733a2f2f692e6962622e636f2f317374676e32382f63726564656e7469616c732e706e67 "this image")

------------


## 2. Generate token.json
1. In the terminal, navigate to Cypress folder and execute the following command: 
```bash
node <node_modules>/gmail-tester/init.js <path-to-credentials.json> <path-to-token.json> <target-email>
```

1. If having no issue, a link will be provided in terminal, go to the given link, login by **target-email** and continue to get the code. Copy that and back to the terminal

1. Paste that code into the terminal, press Enter. If everything is done, the following line will we shown: 
> [gmail] Found!

1. Now **token.json** file is generated and everything is done.
