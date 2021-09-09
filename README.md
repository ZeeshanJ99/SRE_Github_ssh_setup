# SSH setup
- New repository
- select ssh instead of http
- follow the steps on screen



# Creating a webhook
- Navigate to your Github repository's settings page
- select Webhooks
- select Add webhook 
- Under Payload URL input the Jenkins server IP address followed by /github-webhook/
- e.g. `http://18.170.212.241/github-webhhok/`
- Under Content type, select application/json.
- Leave the Secret box empty.
- Select the events that you want to trigger the webhook.
- Check the Active check-box. If this is not added, the webhook will not work.
- Add webhook



## Generate ssh key
In the terminal, input the command:

`ssh-keygen -t rsa -b 4096 -C "johnsmith@gmail.com"`

(Using the same email address that is associated with your Github account)

- It will then prompt you to add a name, if you do not it will provide the name `id_rsa`
- There is no need to create a passphrase
- `ls` can be used to check whether this process has succeeded, you should see two new items keyname and keyname.pub

![image](https://user-images.githubusercontent.com/88186084/132696603-870bd702-34b9-4880-8044-8ebae7a9325e.png)


-----------------------------------------------

## Deloying .pub to github
- Navigate to Github settings
- `SSH and GPG keys`
- `New ssh key`
- name the key
- within the terminal `cat` into your generated `.pub` key from above
- copy all the text and paste it onto the github key section
