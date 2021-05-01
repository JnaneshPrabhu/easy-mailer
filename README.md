# Easy Mailer
## _One Click send mail using all popular mailing_





Easy Mailer is an easy to use one line method to send mails using authentication of all popular services like google,outlook, etc



## Features

- Allows to send multiple attachments over mail (Note size limit of mailer applies)
- One line call to function to send mail
- Works on outlook mailer as of now.
- Google, Yahoo, Rediff soon to be added.
- Option to send any kind of attachment over mail.
- Customisable subject line and body of the mailer.



## Installation

Easy mailer requires python3 and above to run. Python 2 compatible but not tested.

Install the package via pip.

```sh
pip install easy-mailer
```

For forking directly from git...

```sh
pip install git+https://github.com/JnaneshPrabhu/easy-mailer.git
```

This takes into input parameters as shown below

    Args:
        username: required
            type: str
            The email id of outlook from which one needs to send an email.
        password: required
            type: str
            Password of outlook email for authentication.
        recipient list:
            type: list
            The recipients enclosed in a list
        subject: required
            type: str
            The subject line of the mailer
        message: optional
            type: str
            Any text to be displayed in body of the mailer. Please provide absolute local path of the attachment.
        files: optional
            type: Any
            Attachments to be uploaded in the mailer. Note mail restrictions of memory still applies.
        filenames: optional, required in case files are provided.
            type: List of str
            Applicable only when files is not empty.
            Pass on the list containing names of files one wants to display in the mail body. By default will show processed absolute path names.
            

    Returns:
        A mail is sent to intended recipients. Can be used to automate sending of mails/reports.


Open your favorite Terminal and run these commands.



```sh
from easy_mailer import send_mail
```


```sh
send_mail(username = 'abc@email.com', password = 'pass', subject = 'Sample Subject')
```

If one wants to have attachments use following:
```sh
send_mail(username = 'abc@email.com', password = 'pass', subject = 'Sample Subject', files = ['<abs_path_of_file1>','<abs_path_of_file2>'],filenames = ['display_name_1','display_name_2'])
```
Its important to note here that files will contain **absolute path names** whereas filenames will contain **name of the file to be displayed in mailer**.
By default the absolute path will be considered. 

## License

MIT



