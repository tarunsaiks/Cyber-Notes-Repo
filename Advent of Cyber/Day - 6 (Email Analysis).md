
## What is Email Analysis

The process of extracting the email header information to expose the email file (.eml) details

It contains technical details like sender, recipient, path, return address and attachments. These fields are closely analysed to determine if the email is suspicious or legitimate. So the email can be filtered/quarantined using some tools.


![[Your_Account_has_been_locked.eml]]
| Field Name | Description| Example |
| ------------- | ------------ | --------- |
| From | The sender's address | amazon@zyevantoby.cn |
 | To | The reciever's address (including CC and BCC) | saintington73@outlook.com
 | Date | Timestamp, when the email was sent | Wed, 14 Jul 2021 01:40:32 +0900
 | Subject | The subject of the email | Your Account has been Locked
 | Return Path | The return address of the reply (Reply - To)(If you reply, the return address will be as defined in here) | amazon@zyevantoby.cn
 | Domain Key and DKIM Signatures | Email signatures are provided by email services to identify and authenticate emails |  (DKIM-Signature) Check inside the .eml file
 | SPF | Shows the server that was used to send the email (This will help understand if the actual server is used to send the email from a specific domain) |
 | Message-ID | Unique ID of the email  | Message-ID: <000756bf516d$9bad2034$6e61f7fb$@vinuqou>
 | MIME-Version | Used MIME Version | MIME-Version: 1.0
 | X-Headers | The reciever mail providers usually add these fields. Provided Info is usually experimental and can be different according to mail provider |
