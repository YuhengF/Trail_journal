I used claude to write this app to track my personal hiking record. I tried to include all functionalities I feel excited about (especially those not included by popular hiking apps, for example showing all past trails altogether on the map, which gives people sometimes sense of achievements as if they're wandering in their kindom of hiking realm). Bugs might exist, please feel free to leave a message for any comments or suggestions. 

## To use this app

### If you don't want to touch any programming work:

1. You can use my existing github page session **https://yuhengf.github.io/Trail_journal/**. In order to sync your data, you need to contact me to create a private data repo for you under my github account. If you don't enable Sync you can still use the app but then all data files will be saved locally on a single device (you can export the json and import it on other devices but it's a bit of hassle);
2. To establish Sync, in your first time usage (or on a new device): visit the app webpage **https://yuhengf.github.io/Trail_journal/** -> Click Sync (bottom left) -> enter four pieces of info: my github user name (YuhengF), the private data repo (I will tell you what is, something like "data_tom"), the token I give you (will be a very long string), data file path (default is data.json which is good; you can also name it your own way if you understand what .json kinda means, and it should be the same throught out the whole usage across devices) -> optional encrytion (**I won't be able to see your content at all after encrytion. User has to remember their passphrase otherwise they will forever lose access to their data**). You need to fill the same information again everytime you want to use it on a new device;
3. To create new trails you can either draw on the map (this is an exciting tiny functionality I like about my app), or you need .GPX files (.GPX is a GPS data format). One way to obtain .GPX is to export apple watch health data (you can easily find your workout routes in .GPX format in the exported zip).


### If you want to do everything yourself:

1. Fork the repo;
2. Make sure it's set to public so you can enable **Page** function on github;
3. Create your own private data managing repo (say "my_data") on your own github, and then enable a fine-grained token to access this my_data repo;
4. In the first time setup of the app, access the page hosting this trail journal html (would be something like https://yuhengf.github.io/Trail_journal/ but under your own github), and then click **sync** button. Fill in the token etc info to access your private data;
5. The trails data rely on GPX files (.GPX is a GPS data format). One way to obtain it is to export apple watch health data (you can easily find your workout routes in GPX format in the exported zip).

## Why I save the data in this way:
Just so I don't need any server or datasync services other than github. There're a million of other ways, but this way is the most viable if someone wants to deploy this app when they have and only have a github account.
Next step to simplify for new user. I need to wrap things up using only account name and passphrase.


## Notes for myself or users who want to know how I store their data under my github account:

1. Create private repo, say, named "data_tom". Then create fine-grained token to access this data repo (under Developer Settings -> Personal access tokens (Fine-grained tokens) -> Generate new token -> Token name, appropriate expiration time -> only selected repo -> select that private data repo for user -> Add permissions -> contents -> read and write -> done -> send that token to user);

