# PIAIC-Bootcamp2020-Class1

Deploying a simple static webpage on **Surge.sh**

---

### How to install Surge and Deploy your Project

- First ensure you have latest version of [Node.js](https://nodejs.org/en/) installed.

- Then type this command `npm install --global surge` on `Linux Terminal` or `Windows Command Prompt/ Windows PowerShell`.

- After installation process, cd (change directory) to your project repository/folder.

- Type `surge` and press enter key. Type email and password to create or login into your account.

- After logging in, surge will ask you to confirm your repository where the project is located.

- Next surge will ask for domain name. It will suggest you one but you can have your own but it should end with surge.sh

- If your domain name already exit it will give you an error that domain already exits otherwise it will published your project on specfied domain name.

- And that is it. Your project is up and running.

- Following are some scenarios and useful commands that will help you alot.

  - Suppose, you updated your project and want to redeploy. Naturally you want to update on the same domain which you already created. You can do this in two ways.

    - One way is, Type `surge --domain sampleproject.surge.sh` into command line. Make sure you are in project directory/root folder. This command will redeploy your updated changes to already existed domain. There is one catch you have to remember the domain name and have to type everytime updating your project.

    - Second method is, Type `echo sampleproject.surge.sh > CNAME`. This command will create `CNAME` file into root directory of your project and contains domain name which you don't have to remember. Once `CNAME` file is created just type `surge` rather than typing domain name and it will update your project. I prefer second way as i can check `CNAME` file on any project to find out the domain name.

  - `surge list` command will show all your domains which are hosted on Surge CDN.

  - If you want to delete a domain `surge teardown sampleproject.surge.sh` command will remove domain permanently. If no domain is passed in, Surge will check for a CNAME file to use. Otherwise, it will promt you the domain you would like to teardown.
