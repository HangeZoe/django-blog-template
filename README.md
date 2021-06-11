# Very simple blog template on Django
You can read this instruction on [English](https://github.com/HangeZoe/django-blog-template#deploy-this-blog-on-pythonanywhere), [Russian](https://github.com/HangeZoe/django-blog-template#kak-deploit-na-pythonanywhere) or [Czech](https://github.com/HangeZoe/django-blog-template#jak-na-ten-pythonanywhere) languages. 
## Deploy this blog on PythonAnywhere
You can see how the blog works by following the link: https://hangezoe.pythonanywhere.com/
### 0. GitHub account
You must have own GitHub account. If you haven't, when sign up. It's about one minute.
### 1. Fork this repository. 
When you sign in, hit the button "Fork" near the top right. Ok, now you have a copy of this repository! You must have `https://github.com/<your-github-username>/django-blog-template` link.
### 2. Sign up on PythonAnywhere
(you can deploy free with "Beginner" account). Your future blog's URL will take your own nickname `yourusername.pythonanywhere.com`.
### 3. Creating a PythonAnywhere API token. 
Sign in PythonAnywhere => find the link near the top right to your "Account" => select the tab named "API token" => hit the button "Create new API token". 
### 4. Start configuring! 
Go back to the main [PythonAnywhere Dashboard](https://pythonanywhere.com). Choose the option to start a "Bash" console. Don't worry, next tasks about only "Copy&Paste" ;)
### 5. In open console: 
`pip3.8 install --user pythonanywhere`
### 6. In console (don't forget to use your GitHub username in place of <your-github-username>): 
`pa_autoconfigure_django.py --python=3.8 https://github.com/<your-github-username>/my-first-blog.git`
### 7. In console: 
`python manage.py createsuperuser`
When prompted, type your username (lowercase, no spaces), email address, and password. Don't worry that you can't see the password you're typing in – that's how it's supposed to be. Type it in and press enter to continue. The output should look like this (where the username and email should be your own ones):
```
Username: <superusername>
Email address: <anyname@example.com>
Password:
Password (again):
Superuser created successfully.
```
Return to your browser and go to `https://<yourusername>.pythonanywhere.com/admin/`. Log in with the superuser's credentials you chose; you should see the Django admin dashboard.
### 8. That's all! Congrats! :)

Of course, you will to change my scary design in future ;) Whenever you make changes to your CSS files (static files), you need to run command on the console for update them: `python manage.py collectstatic`.
