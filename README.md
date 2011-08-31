GiGit
===

It's a shell script that creates a Git deployment environment to deploy content from a staging repo to a production site


### And who made that thing ###

Me, well technically thanx to the world wide web, I gathered knowledge from some smart and some dumb people online.

So you can get in touch with me [@Mardix](http://twitter.com/mardix) or here on Github -> [Mardix](http://github.com/mardix)

---  

### But why GiGit though? 

As a web developer it's always a hassle to publish pages via FTP, specially if there are a lot of changes.

Thanks to Git, I can say good bye to FTP. (For real!). 

I made this script for my personal projects, and released it under the MIT license for anyone who may need it for their own project


---


### Install ###


Installing GiGit is pretty straight forward.

1. Clone this repo over to your environment
2. `cd GiGit`
3. `chmod +x gigit`


### Create the environment  ###

 `cd GiGit`

 `./gigit -f -s "StagingRepo" -p "ProductionDir" -n "DeployName"`


#### Params

> -f : force it to create folders and repos that don't exist
   
> -s || --staging : The staging directory name from $HOME

> -p || --production : The production directy where the files will be pushed from staging to development

> -n || --name : The name of the deployment. Will be used to create the bare repo

> -h || --help : The help menu


### How to deploy ###

1. Push your changes to the Staging Repo with your normal `git push`
2. Then execute ./$DeployName.git/gigit-deploy 
It will copy your changes from Staging to Production and you are done!


#### A simple Example 

Let's say you a site www.mysite.com in the folder /public_www

You setup a staging environment stage.mysite.com in the folder /public_stage

After you push changes to stage.mysite.com, you want to publish them to www

So copy GiGit into your $HOME directory

`./gigit -f -s "public_stage" -p "public_www" -n "web"`


Now after you push your changes to public_stage

you can run: `./web.git/gigit-deploy` 

It will copy over the changes from `public_stage` to `public_www`


That's it!

 



