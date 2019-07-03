####Git log graph config 

add content below to your .gitconfig file. 

 

[alias] 

lg1 = log --graph --abbrev-commit --decorate --date=relative --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all 

 

lg2 = log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold cyan)%aD%C(reset) %C(bold green)(%ar)%C(reset)%C(bold yellow)%d%C(reset)%n'' %C(white)%s%C(reset) %C(dim white)- %an%C(reset)' --all 

 

lg3 = log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %Cblue<%an>%Creset' --abbrev-commit --date=relative --all 

 

lg = !"git lg2" 

 

st = status 

----
![avatar](https://github.com/tjlcast/Note_Git/blob/master/imgs/GetImageAttachment%20(1).png)
![avatar](https://github.com/tjlcast/Note_Git/blob/master/imgs/GetImageAttachment%20(2).png)
![avatar](https://github.com/tjlcast/Note_Git/blob/master/imgs/GetImageAttachment%20(3).png)
