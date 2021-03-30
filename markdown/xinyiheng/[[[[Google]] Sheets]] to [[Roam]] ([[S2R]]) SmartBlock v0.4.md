- # INSTRUCTIONS (^^MUST READ^^)
    - ## Setup your Personal [[API]] for [[[[Google]] Sheets]]
        - ^^NOTE:^^ You only have to go through this process one time. Going forward, SmartBlocks will use the Refresh Token generated from this process to authenticate each time.
        - Go to this link: https://console.developers.google.com/
        - Register for [[[[Google]] Cloud Platform]] if you haven't already (it will pop up a notice if so)
            - #screenshot
                - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fsamdynamics%2FdhCQ004lVd.png?alt=media&token=954c1434-9530-4620-b5cf-cd8fd734e428)
        - Create a New Project by selecting `Select a Project` > `New Project`
            - #screenshot
                - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fsamdynamics%2FqLwb_IQ3Va.png?alt=media&token=d82f82fe-640b-484f-81fc-a06b17b08a13)
        - Name the project whatever you want.
            - I called it **Sheets to Roam**
            - You can ignore the Location / Organization leaving it as __No Organization__
            - Click `CREATE`
            - #screenshot
                - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fsamdynamics%2Fg5lwmrMz-Y.png?alt=media&token=2299a26e-280d-4b5b-9a77-421bff66a2f6)
        - It takes 10-20 seconds to create your project. Once completed, select the project you just created.
            - Select `Select a Project` > **Sheets to Roam** (or whatever you named it)
            - #screenshot
                - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fsamdynamics%2FPd5ZYM_O-F.png?alt=media&token=99b36c33-6e9e-4d8a-a7ce-5bb75314e0ec)
        - Enable the #[[[[Google]] Sheets]] #API
            - Screenshots for this entire process are below --> #screenshot for this entire section.
            - Select the `ENABLE APIS AND SERVICES` up top
            - Search for __sheets__ and then select **Google Sheets API**
            - Select `ENABLE` and it should take you to an `Overview` page for the #API
            - Select `Credentials` on the left side and `CREATE CREDENTIALS` at the top and then `OAuth client ID`
            - On the right click the button that says `CONFIGURE CONSENT SCREEN` and apply the following settings:
                - Select `External` and then `CREATE`
                - Fill out the following for App Info and App domain:
                    - Name the App whatever you want.
                        - I called it **Sheets to Roam App**
                    - Click the dropdown for `User support email` and select your email
                    - Ignore the logo
                    - Ignore the whole section for **App domain** (leave them blank)
                    - Ignore the **Authorized domains** section as well
                    - Enter your email address in the **Developer contact information** section
                - Select `SAVE AND CONTINUE` at the bottom of the page
                - Scopes
                    - Select the button: `Add or Remove Scopes`
                    - Select the Google Sheets API > .../auth/spreadsheets Scope
                        - The description says: "__See, edit, create, and delete your spreadsheets in Google Drive__"
                    - Select `UPDATE` button at the bottom
                    - The __spreadsheets__ scope should now show up under the **Your sensitive scopes** section.
                - Select `SAVE AND CONTINUE` at the bottom of the page
                - Select `ADD USERS` under the **Test users** section and add your email
                - Select `SAVE AND CONTINUE` at the bottom of the page
            - Now the Consent Screen has been created and you should see a Summary Screen
            - Select `Credentials` on the left side and `CREATE CREDENTIALS` at the top and then `OAuth client ID` (as you did previously)
            - Select **Web application** for the `Application type`
            - Name it whatever you want (I left the default as **Web client 1**)
            - Leave the `Authorized JavaScript origins` blank
            - For the `Authorized redirect URIs` click `ADD URI` and enter the following:
                - http://localhost:8080
            - Click the `CREATE` button
            - A pop-up will appear showing you your **Client ID** and **Client Secret** - Copy both of these into your Roam Graph somewhere to be used later (can use the following blocks if you'd like)
                - Your Client ID: 1015985963461-a9m8h3htgiqq6k6glieoqq56hqake5qi.apps.googleusercontent.com
                - Your Client Secret: dUATkYFteFmqIqwkhNWK29bU
            - Now you can move to the next section --> Get your Google [[API]] Auth Code
            - #screenshot for this entire section.
                - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fsamdynamics%2FFnXY6RejMJ.png?alt=media&token=84dcb4e4-0110-4bf9-9ffe-591e37479431)
                - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fsamdynamics%2Fyl1s0XqAYf.png?alt=media&token=50aa2598-d520-404d-8e6e-b57d7a43e834)
                - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fsamdynamics%2FK_xCAR-nwl.png?alt=media&token=2f4ca23f-615a-499b-ad0b-53ad4d5241f5)
                - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fsamdynamics%2FEfF7DrHjc1.png?alt=media&token=d6c4a7cf-a926-4c80-9dd3-fc921f17a30b)
                - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fsamdynamics%2Fa5piFdPkpM.png?alt=media&token=3671c9d2-33b7-4b89-a1ef-c88e28bbc52a)
                - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fsamdynamics%2FmJuTUFOaQ9.png?alt=media&token=f29f4abb-1739-43b4-82d4-7e8e1eab7cbd)
                - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fsamdynamics%2FdUwIlGvwLd.png?alt=media&token=0c420724-fdf9-4232-b85c-cfd42315a6cf)
                - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fsamdynamics%2FvAzUO5X2Y8.png?alt=media&token=990ba44f-f8de-42d3-a318-cdf583ecc8ad)
                - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fsamdynamics%2Ff9ky2DGQtb.png?alt=media&token=b9432bef-daf2-41e8-840b-19ed49539ba8)
                - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fsamdynamics%2FQe1oHuFs8S.png?alt=media&token=2e21fdae-c184-443a-93df-d7fc11a639e0)
                - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fsamdynamics%2Fc6zJRhJ-H6.png?alt=media&token=6bb925d3-e21c-4f58-9d03-353d4db7fae6)
                - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fsamdynamics%2FEfF7DrHjc1.png?alt=media&token=d6c4a7cf-a926-4c80-9dd3-fc921f17a30b)
                - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fsamdynamics%2FMRgv08e55w.png?alt=media&token=222112bc-91d0-4dd9-bd07-eee2986a916c)
                - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fsamdynamics%2FywN3iMTrhl.png?alt=media&token=e7326ff6-3991-44f9-86f1-cd9a02c66ddc)
    - ## Get your Google [[API]] Auth Code
        - Add your **Client ID** to the end of the following URL:
            - https://accounts.google.com/o/oauth2/v2/auth?scope=https%3A//www.googleapis.com/auth/spreadsheets&access_type=offline&include_granted_scopes=true&response_type=code&redirect_uri=http%3A//localhost:8080&client_id=1015985963461-a9m8h3htgiqq6k6glieoqq56hqake5qi.apps.googleusercontent.com
        - Now click the link above (after adding your **Client ID** to it).. it should start the #Google authentication / approval process.
        - Sign-in with your #Google account (if it asks you to)
        - You may get an error / warning like the following:
            - #screenshot
                - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fsamdynamics%2FixNO7GuKLd.png?alt=media&token=01569fbc-80a2-4039-a211-609e0872d099)
            - This is normal and expected as you are not publishing your Google App... you are just using it in "Test Mode" for your own personal use.
            - Click the link: **Advanced**
                - #screenshot
                    - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fsamdynamics%2FYYI7gOT936.png?alt=media&token=df795230-6fbb-4244-bd63-8e3b7e087093)
            - Click the link: **Go to Sheets to Roam App** (or whatever you named your App)
                - #screenshot
                    - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fsamdynamics%2Fs7AszKZQNE.png?alt=media&token=1d6f4cac-8726-487a-a1e6-9d3c3b756d59)
            - I know this seems "shady" but remember you created this App yourself. It is doing nothing else but trying to connect to your newly created "App" API and even provides your email address in the warnings.
        - You should receive a pop-up asking you to Grant permissions. Click `Allow`.
            - #screenshot
                - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fsamdynamics%2FIyBSOfNjkv.png?alt=media&token=55d9adda-3662-4823-8c08-3850c8a5e105)
        - Click `Allow` one more time to confirm approval / authentication to your App API
            - #screenshot
                - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fsamdynamics%2FwQGuL8YYMe.png?alt=media&token=201495e6-3603-4969-83f0-e8df0647f40c)
        - Now the ^^IMPORTANT^^ part. It looks like the page/process errored out. But this is expected as we don't have an actual server side App to redirect to.
            - #screenshot
                - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fsamdynamics%2FCJd5Y1bBq8.png?alt=media&token=0bcf512d-4b21-46ed-8bb9-8a4a97392ac4)
            - What we need is the Auth **Code** from the resulting URL shown in your web browser.
            - Copy the entire URL into the block below:
                - Your URL: http://localhost:8080/?code=4/0AY0e-g5zztrjLOioLUz-OTP3LLQqTqnOgD0UrQrponlktgtOZ0A7IBW6WuZJaV9kKN5dJg&scope=https://www.googleapis.com/auth/spreadsheets
                - EXAMPLE:
                    - http://localhost:8080/?code=4/xyz-abc-jlajsldfjasldjfjkXXXXXXXXXXXXXXXXXXXXXXXX&scope=https://www.googleapis.com/auth/spreadsheets
            - Extract out just the Auth **Code** from the URL
                - ^^Your Auth Code^^: 4/0AY0e-g5zztrjLOioLUz-OTP3LLQqTqnOgD0UrQrponlktgtOZ0A7IBW6WuZJaV9kKN5dJg
                - EXAMPLE:
                    - http://localhost:8080/?code=^^4/xyz-abc-jlajsldfjasldjfjkXXXXXXXXXXXXXXXXXXXXXXXX^^&scope=https://www.googleapis.com/auth/spreadsheets
                    - Example Auth Code: 4/xyz-abc-jlajsldfjasldjfjkXXXXXXXXXXXXXXXXXXXXXXXX
        - If for whatever reason you lost your code or closed the window without writing it down, you need to start the process over starting by clicking the link from this step --> Now click the link above (after adding your **Client ID** to it).. it should start the #Google authentication / approval process.
    - ## Authenticate to API for the first time
        - Now you are ready to start using the Google Sheets SmartBlocks
        - First you must setup the #42SmartBlock S2R - Refresh Token SmartBlock ^^by updating the following^^:
            - Replace the following in the block embed `ENTER_YOUR_CLIENT_ID` with your **Client ID** from earlier in the process --> Your Client ID: 1015985963461-a9m8h3htgiqq6k6glieoqq56hqake5qi.apps.googleusercontent.com
                - <%SET:gshClientId,1015985963461-a9m8h3htgiqq6k6glieoqq56hqake5qi.apps.googleusercontent.com%><%NOBLOCKOUTPUT%>
            - Replace the following in the block embed `ENTER_YOUR_CLIENT_SECRET` with your **Client Secret** from earlier in the process --> Your Client Secret: dUATkYFteFmqIqwkhNWK29bU
                - <%SET:gshClientSecret,dUATkYFteFmqIqwkhNWK29bU%><%NOBLOCKOUTPUT%>
            - Replace the following in the block embed `ENTER_YOUR_AUTH_CODE` with your **Auth Code** from earlier in the process --> ^^Your Auth Code^^: 4/0AY0e-g5zztrjLOioLUz-OTP3LLQqTqnOgD0UrQrponlktgtOZ0A7IBW6WuZJaV9kKN5dJg
                - <%SET:gshAuthCode,4/0AY0e-g5zztrjLOioLUz-OTP3LLQqTqnOgD0UrQrponlktgtOZ0A7IBW6WuZJaV9kKN5dJg%><%NOBLOCKOUTPUT%>
        - Now run the #42SmartBlock S2R - Refresh Token SmartBlock.
            - Run it here    1//06Ku1V_w5bKG1CgYIARAAGAYSNwF-L9IrP_avBgQNPPnTmyvCVKDsBIOdz9jM51EGo1kPYJdA0MkAfL4HSawRyjMRmMIKqzT6D_Y
            - The result of this SmartBlock will return your **Refresh Token** to be used to authenticate with SmartBlocks going forward.
            - Replace the following in the block embed `ENTER_YOUR_REFRESH_TOKEN` with your **Refresh Token** generated by the SmartBlock you just ran.
                - <%SET:gshRefToken,1//06Ku1V_w5bKG1CgYIARAAGAYSNwF-L9IrP_avBgQNPPnTmyvCVKDsBIOdz9jM51EGo1kPYJdA0MkAfL4HSawRyjMRmMIKqzT6D_Y%><%NOBLOCKOUTPUT%>
            - If all goes well, you will NOT have to run this SmartBlock ever again. The Refresh Token will be used to Authenticate each time and never expires unless you revoke it or change your password in #Google.
            - Now you ^^ALSO need to add^^ your **Client ID** and **Client Secret** one more time:
                - Replace the following in the block embed `ENTER_YOUR_CLIENT_ID` with your **Client ID** from earlier in the process --> Your Client ID: 1015985963461-a9m8h3htgiqq6k6glieoqq56hqake5qi.apps.googleusercontent.com
                    - <%SET:gshClientId,1015985963461-a9m8h3htgiqq6k6glieoqq56hqake5qi.apps.googleusercontent.com%><%NOBLOCKOUTPUT%>
                - Replace the following in the block embed `ENTER_YOUR_CLIENT_SECRET` with your **Client Secret** from earlier in the process --> Your Client Secret: dUATkYFteFmqIqwkhNWK29bU
                    - <%SET:gshClientSecret,dUATkYFteFmqIqwkhNWK29bU%><%NOBLOCKOUTPUT%>
        - Now you are ready to Authenticate for the first time and start using the #S2R Integration!
        - Run the SmartBlock #42SmartBlock S2R - Authenticate
            - When you run it, if successful, it should return **Authentication successful!**  Authentication successful!
            - You are now ready to start using #S2R by starting here --> Using #S2R SmartBlocks to interact with #[[[[Google]] Sheets]] for the first time
            - ^^Note:^^ you need to re-authenticate by simply running this #42SmartBlock S2R - Authenticate SmartBlock whenever the google OAuth session expires (usually after one hour of usage)... or when/if you receive an authentication error.
                - It does NOT require you to sign-in or do anything further.
                - Just simply re-run the SmartBlock each time you need to re-authenticate.
                - All the steps above with the creation of the API and getting the Auth Code and Refresh Token etc. do NOT have to be done again unless you revoke the API and/or change your Google password.
- # DEMO
    - ## Using #S2R SmartBlocks to interact with #[[[[Google]] Sheets]] for the first time
        - I recommend creating a test page to start with an empty/blank page to easily test from.
        - ^^WATCH THIS video recording^^ using the below sample data to help you get started (click the link to open the MP4 in a browser tab to view it):
            - https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fsamdynamics%2FboYNU43MKE.mp4?alt=media&token=beebe672-8aa1-41df-84b1-56eceb41c5c9
        - The spreadsheet below is a Public test spreadsheet so you are welcome to use it to test as well.
        - Copy the following sample data to the top of the test page you created:
            - Test #[[[[Google]] Sheets]] Spreadsheet:
                - https://docs.google.com/spreadsheets/d/1htjj5HjVe0XXTH-vIa4hil-hhn3pd5GtQY8rNp2WSRI/edit#gid=17193194
            - Highlighting the Spreadsheet ID and the Sheet GID so that you know where to look for them:
                - https://docs.google.com/spreadsheets/d/^^ 1htjj5HjVe0XXTH-vIa4hil-hhn3pd5GtQY8rNp2WSRI ^^/edit#gid=^^ 17193194 ^^
            - S2R Spreadsheet ID:: 1htjj5HjVe0XXTH-vIa4hil-hhn3pd5GtQY8rNp2WSRI
            - S2R Sheet GID:: 17193194
            - Some test/demo data:
                - A3 #S2R
                    - NEED TO START WITH A CHILD BLOCK UNDERNEATH EACH CELL REFERENCE. THIS IS WHERE THE VALUE YOU PULL FROM SHEETS WILL GO FOR `A3` FOR EXAMPLE.
                - B5 #S2R
                    - 
                - B7 #S2R
                    - 
                - E10 #S2R
                    - 
        - After adding the #[[S2R Spreadsheet ID]] and #[[S2R Sheet GID]] to their respective attribute blocks
            - along with some cell references with the #S2R tag
            - each having a child block created underneath each cell reference block
                - Example:
                    - C5 #S2R
                        - 
                    - E2 #S2R
                        - 
            - you are ready to pull values from Sheets into Roam by running the SmartBlock --> #42SmartBlock S2R - Pull Data from Sheets
        - When you want to change a value in Roam and update/push the change to Sheets, simply change the value in the child block underneath a cell reference block and run the SmartBlock --> #42SmartBlock S2R - Push Data to Sheets
        - Both the Pull and Push SmartBlocks will run for all visible blocks on the page you are currently on (that have a #S2R tag) at the time you run the SmartBlock.
        - If a cell in #[[[[Google]] Sheets]] is a formula cell, the #S2R `Push` SmartBlock will NOT overwrite / update it regardless of what you change the block to in Roam.
        - ^^WARNING:^^ I have not tested on pages open in the sidebar. For now, just use the #S2R SmartBlocks on the left side "main page".
    - ## Tips and Tricks
        - While the default is to use the cell references with the specific **Sheet** that you targeted with the **S2R Sheet GID** attribute value, you can also pull/push from/to cells from other sheets.
            - Simply add the sheet name followed by an `!` in front of the cell reference.
            - For Example:
                - Sheet3!C5 #S2R
                - #screenshot
                    - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fsamdynamics%2FC7otautSN8.png?alt=media&token=a3b6ddd8-dad8-49c1-b621-6757b6a0a58a)
            - If there is no sheet listed in front of a cell reference then it defaults to the sheet referenced in the **S2R Sheet GID** attribute value.
            - #MP4 #Demo
                - https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fsamdynamics%2F3uuIgocs0B.mp4?alt=media&token=143768c7-ae98-40dc-bca3-986697f60443
                - 
        - If you collapse a parent block with cell references underneath it, they will NOT push/pull with SmartBlocks.
            - Blocks will only run/push/pull if they are:
                - 1) Visible on page
                - 2) have a #S2R tag
            - #MP4 #Demo
                - https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fsamdynamics%2F3uuIgocs0B.mp4?alt=media&token=143768c7-ae98-40dc-bca3-986697f60443
        - You can use Block References in Roam as the source to `Push` to Sheets. It will resolve the value of the Block Reference and use that to `Push` / Update the cell in Sheets.
            - EXAMPLE:
                - B20 #S2R - INPUT
                    - The value for this block ref will be resolved and then PUSHED to Sheets.
                - Non S2R block that won't be used when SmartBlock runs.
                    - Here is a block from my graph I can reference as the value for S2R above in cell B20:
                        - The value for this block ref will be resolved and then PUSHED to Sheets.
                - **NOTE:** Any S2R Roam blocks that are using a block reference will NOT be overwritten by data from Sheets when you run the `Pull` SmartBlock.
    - ## Various #MP4 video DEMOs / Guides / Examples
        - Intro Demo:
            - https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fsamdynamics%2Fh0yIDO3Czg.mp4?alt=media&token=16cb4aab-d95f-4e1c-af59-51228d5ace82
        - Fun / Simple Vlookup example Demo:
            - https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fsamdynamics%2FKb6eS88ntx.mp4?alt=media&token=08328683-e8af-49c9-8db0-f1e5d4ceff29
        - Reference and `Push` / `Pull` blocks in other sheets; not just the one named in the **S2R Sheet GID:** attribute block. Also can hide cell reference blocks in Roam from being `Pushed` or `Pulled` by collapsing parent blocks.
            - https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fsamdynamics%2FBZwm8tXL1x.mp4?alt=media&token=f0c54342-5440-4bb6-9636-924fd5921bd9
        - When using the `Push` SmartBlock, if a cell is a formula in Sheets, it will also `Pull` it back.
            - This Demo shows ability to use an INPUT block to `Push` to Sheets and then at the same time return the result from a Sheets formula in another cell reference block.
            - Great for Vlookups!
            - https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fsamdynamics%2Fe9egy_xWbb.mp4?alt=media&token=b604ac1c-631e-4785-9d3f-8c9b5dc84070
        - Use Block References in Roam to populate values to `Push` to Sheets:
            - Even when `Pulling` from Sheets, a cell reference block in Roam with a Block Reference will NOT be overwritten.
            - https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fsamdynamics%2Fhf2xZyyDoF.mp4?alt=media&token=015ffb55-d591-4d64-9fda-e3bb54133da5
- # SMARTBLOCKS
    - #42SmartBlock S2R - Refresh Token
        - <%SET:gshClientId,1015985963461-a9m8h3htgiqq6k6glieoqq56hqake5qi.apps.googleusercontent.com%><%NOBLOCKOUTPUT%>
        - <%SET:gshClientSecret,dUATkYFteFmqIqwkhNWK29bU%><%NOBLOCKOUTPUT%>
        - <%SET:gshAuthCode,4/0AY0e-g5zztrjLOioLUz-OTP3LLQqTqnOgD0UrQrponlktgtOZ0A7IBW6WuZJaV9kKN5dJg%><%NOBLOCKOUTPUT%>
        - <%JA:
```javascript

var gshClientId = roam42.smartBlocks.activeWorkflow.vars["gshClientId"];
var gshClientSecret = roam42.smartBlocks.activeWorkflow.vars["gshClientSecret"];
var gshAuthCode = roam42.smartBlocks.activeWorkflow.vars["gshAuthCode"];
var requestResults = await fetch('https://oauth2.googleapis.com/token', {
    method: 'POST',
    headers: { 'Content-Type': 'application/x-www-form-urlencoded' },
    body: 'code=' + gshAuthCode + '&client_id=' + gshClientId + '&client_secret=' + gshClientSecret + '&redirect_uri=' + 'http://localhost:8080' + '&grant_type=' + 'authorization_code'
});

var dataResults = await requestResults.json();

if (dataResults["refresh_token"]) {
    return dataResults["refresh_token"];
}
else {
    return dataResults["error"] + ': ' + dataResults["error_description"];
}
```
%>
    - #42SmartBlock S2R - Authenticate
        - <%SET:gshClientId,1015985963461-a9m8h3htgiqq6k6glieoqq56hqake5qi.apps.googleusercontent.com%><%NOBLOCKOUTPUT%>
        - <%SET:gshClientSecret,dUATkYFteFmqIqwkhNWK29bU%><%NOBLOCKOUTPUT%>
        - <%SET:gshRefToken,1//06Ku1V_w5bKG1CgYIARAAGAYSNwF-L9IrP_avBgQNPPnTmyvCVKDsBIOdz9jM51EGo1kPYJdA0MkAfL4HSawRyjMRmMIKqzT6D_Y%><%NOBLOCKOUTPUT%>
        - <%JA:
```javascript

var gshClientId = roam42.smartBlocks.activeWorkflow.vars["gshClientId"];
var gshClientSecret = roam42.smartBlocks.activeWorkflow.vars["gshClientSecret"];
var gshRefToken = roam42.smartBlocks.activeWorkflow.vars["gshRefToken"];

var requestResults = await fetch('https://oauth2.googleapis.com/token', {
    method: 'POST',
    headers: { 'Content-Type': 'application/x-www-form-urlencoded' },
    body: '&client_id=' + gshClientId + '&client_secret=' + gshClientSecret + '&refresh_token=' + gshRefToken + '&grant_type=' + 'refresh_token'
});

var dataResults = await requestResults.json();
if (dataResults["access_token"]) {
    roam42.smartBlocks.activeWorkflow.vars["gshAccessToken"] = dataResults["access_token"];
    return 'Authentication successful!';
}
else {
    return dataResults["error"] + ': ' + dataResults["error_description"];
}
```
%>
    - #42SmartBlock S2R - Pull Data from Sheets
        - <%J:
```javascript

var startingContents = roam42.smartBlocks.activeWorkflow.startingBlockContents;
startingContents = startingContents.trim();
document.activeElement.value = '';
if(startingContents == ''){startingContents = ' ';}
return startingContents;
```
%>
        - <%JA:
```javascript

var currentPage = document.title;
var ACCESS_TOKEN = roam42.smartBlocks.activeWorkflow.vars["gshAccessToken"];
if(!ACCESS_TOKEN){ACCESS_TOKEN = '12345';}

var SHEET_ID = '';
var findSheetAttr = document.querySelectorAll("[data-page-links='[\"S2R Spreadsheet ID\"]'] > .rm-block-main [id*='body-outline']")
if (findSheetAttr.length > 0) {
    var sheetIdText = findSheetAttr[0].innerText.trim();
    if (sheetIdText.length > 25) { SHEET_ID = sheetIdText.split('ID:')[1].trim() }
}
if(SHEET_ID == '')
{
    eachBlockTextArea = document.querySelectorAll(".rm-block-input").item(0);
    await setNewValue(eachBlockTextArea, 'You did not enter a **S2R Spreadsheet ID** as a Roam attribute value. If you did, make sure it is visible on the page and not collapsed or hidden from view due to focus/zoom. EXAMPLE: S2R Spreadsheet ID`::` 123456789abcdefghiXXXXXXXX');
    return '';
}

var SHEET_ID_gid = 0;
var findSheetAttr = document.querySelectorAll("[data-page-links='[\"S2R Sheet GID\"]'] > .rm-block-main [id*='body-outline']")
if (findSheetAttr.length > 0) {
    var sheetIdText = findSheetAttr[0].innerText.trim();
    if (sheetIdText.length > 14) { SHEET_ID_gid = sheetIdText.split('GID:')[1].trim() }
}

var SHEET_NAME = '';
var requestResults = await fetch(`https://sheets.googleapis.com/v4/spreadsheets/${SHEET_ID}`,
    {
        headers: {
            "Content-Type": "application/json",
            Authorization: `Bearer ${ACCESS_TOKEN}`
        }
    });

var dataResults = await requestResults.json();
if (dataResults["sheets"]) {
    var sheetFound = dataResults["sheets"].find(sheet => sheet["properties"]["sheetId"] == SHEET_ID_gid);
    if (sheetFound) { SHEET_NAME = sheetFound["properties"]["title"]; }
    else { SHEET_NAME = dataResults["sheets"][0]["properties"]["title"]; }
}
else {
    console.log(dataResults);
    eachBlockTextArea = document.querySelectorAll(".rm-block-input").item(0);
    await setNewValue(eachBlockTextArea, 'ERROR: ' + dataResults["error"]["status"] + ': ' + dataResults["error"]["message"] + ". Most likely just need to run the `S2R - Authenticate` SmartBlock again.");
    return '';
}

async function delay(millis) {
    return new Promise(resolve => setTimeout(resolve, millis));
}

const getMouseEvent = (mouseEventType, buttons) =>
    new MouseEvent(mouseEventType, {
        view: window,
        bubbles: true,
        cancelable: true,
        buttons
    });

async function simulateClick(buttons, element, delayOverride) {
    const mouseClickEvents = ['mousedown', 'click', 'mouseup'];
    mouseClickEvents.forEach(mouseEventType => {
        element.dispatchEvent(getMouseEvent(mouseEventType, buttons));
    });
    return delay(100);
}

async function setNewValue(curBlock, newValue) {
    var nativeInputValueSetter = Object.getOwnPropertyDescriptor(window.HTMLTextAreaElement.prototype, "value").set;
    nativeInputValueSetter.call(curBlock, newValue);
    var ev2 = new Event('input', { bubbles: true });
    curBlock.dispatchEvent(ev2);
    return delay(100);
}

if (currentPage !== 'All Pages' && currentPage !== 'Daily Notes') {
    var allBlocks = document.querySelectorAll("[data-page-links='[\"S2R\"]'] > .rm-block-main [id*='body-outline']");
    var blockCtr = 0;
    for (var i = 0; i < allBlocks.length; i++) {
        var eachBlockDiv = allBlocks.item(i);
        if (eachBlockDiv !== null) {
            await simulateClick(1, eachBlockDiv, 0);
            var eachBlockTextArea = document.querySelectorAll(".rm-block-input").item(0);
            var curValue = eachBlockTextArea.value.toString().trim();
            blockCtr++;
            //Press down arrow to get to cell below
            await roam42KeyboardLib.simulateKey(40, 50);
            eachBlockTextArea = document.querySelectorAll(".rm-block-input").item(0);
            var newValueStr = eachBlockTextArea.value.toString().trim();
            if(/.*\(\(.*\)\).*/.test(newValueStr)){continue;}
            var SHEET_CELL = curValue.substring(0, curValue.indexOf('#S2R')).trim();
            if (SHEET_NAME != '' && SHEET_CELL.indexOf('!') == -1) { SHEET_CELL = SHEET_NAME + '!' + SHEET_CELL; }
            var requestResults = await fetch(`https://sheets.googleapis.com/v4/spreadsheets/${SHEET_ID}/values/${SHEET_CELL}`,
                {
                    headers: {
                        "Content-Type": "application/json",
                        Authorization: `Bearer ${ACCESS_TOKEN}`
                    }
                });
            var dataResults = await requestResults.json();
            if (dataResults["range"]) {
                if (dataResults["values"]) { await setNewValue(eachBlockTextArea, dataResults["values"][0][0].toString()); }
                else { await setNewValue(eachBlockTextArea, ''); }
            }
            else {
                console.log(dataResults);
                await setNewValue(eachBlockTextArea, 'ERROR: ' + dataResults["error"]["status"] + ': ' + dataResults["error"]["message"]);
                return '';
            }
        }
    }
    await simulateClick(1, document.body, 0);
}

return '';
```
%><%NOBLOCKOUTPUT%>
    - #42SmartBlock S2R - Push Data to Sheets
        - <%J:
```javascript

var startingContents = roam42.smartBlocks.activeWorkflow.startingBlockContents;
startingContents = startingContents.trim();
document.activeElement.value = '';
if(startingContents == ''){startingContents = ' ';}
return startingContents;
```
%>
        - <%JA:
```javascript

var currentPage = document.title;
var ACCESS_TOKEN = roam42.smartBlocks.activeWorkflow.vars["gshAccessToken"];
if (!ACCESS_TOKEN) { ACCESS_TOKEN = '12345'; }

var SHEET_ID = '';
var findSheetAttr = document.querySelectorAll("[data-page-links='[\"S2R Spreadsheet ID\"]'] > .rm-block-main [id*='body-outline']")
if (findSheetAttr.length > 0) {
    var sheetIdText = findSheetAttr[0].innerText.trim();
    if (sheetIdText.length > 25) { SHEET_ID = sheetIdText.split('ID:')[1].trim() }
}
if (SHEET_ID == '') {
    eachBlockTextArea = document.querySelectorAll(".rm-block-input").item(0);
    await setNewValue(eachBlockTextArea, 'You did not enter a **S2R Spreadsheet ID** as a Roam attribute value. If you did, make sure it is visible on the page and not collapsed or hidden from view due to focus/zoom. EXAMPLE: S2R Spreadsheet ID`::` 123456789abcdefghiXXXXXXXX');
    return '';
}

var SHEET_ID_gid = 0;
var findSheetAttr = document.querySelectorAll("[data-page-links='[\"S2R Sheet GID\"]'] > .rm-block-main [id*='body-outline']")
if (findSheetAttr.length > 0) {
    var sheetIdText = findSheetAttr[0].innerText.trim();
    if (sheetIdText.length > 14) { SHEET_ID_gid = sheetIdText.split('GID:')[1].trim() }
}

var SHEET_NAME = '';
var requestResults = await fetch(`https://sheets.googleapis.com/v4/spreadsheets/${SHEET_ID}`,
    {
        headers: {
            "Content-Type": "application/json",
            Authorization: `Bearer ${ACCESS_TOKEN}`
        }
    });

var dataResults = await requestResults.json();
if (dataResults["sheets"]) {
    var sheetFound = dataResults["sheets"].find(sheet => sheet["properties"]["sheetId"] == SHEET_ID_gid);
    if (sheetFound) { SHEET_NAME = sheetFound["properties"]["title"]; }
    else { SHEET_NAME = dataResults["sheets"][0]["properties"]["title"]; }
}
else {
    console.log(dataResults);
    eachBlockTextArea = document.querySelectorAll(".rm-block-input").item(0);
    await setNewValue(eachBlockTextArea, 'ERROR: ' + dataResults["error"]["status"] + ': ' + dataResults["error"]["message"] + ". Most likely just need to run the `S2R - Authenticate` SmartBlock again.");
    return '';
}

async function delay(millis) {
    return new Promise(resolve => setTimeout(resolve, millis));
}

const getMouseEvent = (mouseEventType, buttons) =>
    new MouseEvent(mouseEventType, {
        view: window,
        bubbles: true,
        cancelable: true,
        buttons
    });

async function simulateClick(buttons, element, delayOverride) {
    const mouseClickEvents = ['mousedown', 'click', 'mouseup'];
    mouseClickEvents.forEach(mouseEventType => {
        element.dispatchEvent(getMouseEvent(mouseEventType, buttons));
    });
    return delay(100);
}

async function setNewValue(curBlock, newValue) {
    var nativeInputValueSetter = Object.getOwnPropertyDescriptor(window.HTMLTextAreaElement.prototype, "value").set;
    nativeInputValueSetter.call(curBlock, newValue);
    var ev2 = new Event('input', { bubbles: true });
    curBlock.dispatchEvent(ev2);
    return delay(100);
}

if (currentPage !== 'All Pages' && currentPage !== 'Daily Notes') {
    var allBlocks = document.querySelectorAll("[data-page-links='[\"S2R\"]'] > .rm-block-main [id*='body-outline']");
    var blockCtr = 0;
    for (var i = 0; i < allBlocks.length; i++) {
        var eachBlockDiv = allBlocks.item(i);
        if (eachBlockDiv !== null) {
            await simulateClick(1, eachBlockDiv, 0);
            var eachBlockTextArea = document.querySelectorAll(".rm-block-input").item(0);
            var curValue = eachBlockTextArea.value.toString().trim();
            blockCtr++;
            //Press down arrow to get to cell below
            await roam42KeyboardLib.simulateKey(40, 50);
            eachBlockTextArea = document.querySelectorAll(".rm-block-input").item(0);
            var newValueStr = eachBlockTextArea.value.toString().trim();
            var SHEET_CELL = curValue.substring(0, curValue.indexOf('#S2R')).trim();
            if (SHEET_NAME != '' && SHEET_CELL.indexOf('!') == -1) { SHEET_CELL = SHEET_NAME + '!' + SHEET_CELL; }
            var requestResults = await fetch(`https://sheets.googleapis.com/v4/spreadsheets/${SHEET_ID}/values/${SHEET_CELL}?valueRenderOption=FORMULA`,
                {
                    headers: {
                        "Content-Type": "application/json",
                        Authorization: `Bearer ${ACCESS_TOKEN}`
                    }
                });
            var dataResults = await requestResults.json();
            var checkingCurValue = '';
            if (dataResults["range"]) {
                if (dataResults["values"]) { checkingCurValue = dataResults["values"][0][0].toString(); }
                else { checkingCurValue = ''; }
            }
            if (checkingCurValue == newValueStr || checkingCurValue.substring(0, 1) == '=') {
                //Skip if value isn't any different than in Sheets OR if sheets is a formula which we don't want to overwrite
                //If its a formula, then run a PULL command to see if it was updated from a previous PUSH
                if (checkingCurValue.substring(0, 1) == '=') {
                    var requestResults = await fetch(`https://sheets.googleapis.com/v4/spreadsheets/${SHEET_ID}/values/${SHEET_CELL}`,
                        {
                            headers: {
                                "Content-Type": "application/json",
                                Authorization: `Bearer ${ACCESS_TOKEN}`
                            }
                        });
                    var dataResults = await requestResults.json();
                    if (dataResults["range"]) {
                        if (dataResults["values"]) { await setNewValue(eachBlockTextArea, dataResults["values"][0][0].toString()); }
                        else { await setNewValue(eachBlockTextArea, ''); }
                    }
                    else {
                        console.log(dataResults);
                        await setNewValue(eachBlockTextArea, 'ERROR: ' + dataResults["error"]["status"] + ': ' + dataResults["error"]["message"]);
                        return '';
                    }
                }
            }
            else {
                while(/.*\(\(.*\)\).*/.test(newValueStr)) {
                    var findBlockRef = newValueStr.match(/.*(\(\(.*\)\)).*/)[1];
                    var blockRefVal = await roam42.smartBlocks.resolveBlockRef(findBlockRef);
                    newValueStr = newValueStr.replace(findBlockRef,blockRefVal);
                }
                var requestResults = await fetch(`https://sheets.googleapis.com/v4/spreadsheets/${SHEET_ID}/values/${SHEET_CELL}?valueInputOption=USER_ENTERED`,
                    {
                        method: "PUT",
                        headers: {
                            "Content-Type": "application/json",
                            Authorization: `Bearer ${ACCESS_TOKEN}`
                        },
                        body: JSON.stringify(
                            {
                                "range": SHEET_CELL,
                                "majorDimension": "ROWS",
                                "values": [
                                    [newValueStr]
                                    /*
                                    ["Item", "Cost", "Stocked", "Ship Date"],
                                    ["Wheel", "$20.50", "4", "3/1/2016"],
                                    ["Door", "$15", "2", "3/15/2016"],
                                    ["Engine", "$100", "1", "3/20/2016"],
                                    ["Totals", "=SUM(B2:B4)", "=SUM(C2:C4)", "=MAX(D2:D4)"]
                                    */
                                ]
                            })
                    });
                var dataResults = await requestResults.json();

                if (dataResults["updatedRange"]) {
                    //Successful update
                }
                else {
                    await setNewValue(eachBlockTextArea, 'ERROR: ' + dataResults["error"]["status"] + ': ' + dataResults["error"]["message"]);
                    return '';
                }
            }
        }
    }
    await simulateClick(1, document.body, 0);
}

return '';
```
%><%NOBLOCKOUTPUT%>
