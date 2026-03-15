I used claude to write this app to track my personal hiking record. I tried to include all functionalities I feel excited about (especially those not included by popular hiking apps, for example showing all past trails altogether on the map, which gives people sometimes sense of achievements as if they're wandering in their kindom of hiking realm). Bugs might exist, please feel free to leave a message for any comments of suggestions. 

## To use this app

### If you dont want to touch any programming work:

1. You can use my existing github page session **https://yuhengf.github.io/Trail_journal/**, but then all data files will be saved locally on single device if you don't enable Sync. In order to sync your data, you need to contact me to create a private data repo for you under my github account;

### if you want to do everything yourself:

1. Fork the repo
2. Make sure it's set to public so you can enable **Page** function on github;
3. Create your own private data managing repo (say "my_data") on your own github, and then enable a fine-grained token to access this data;
4. In the first time setup of the app, access the page hosting this trail journal html (would be something like https://yuhengf.github.io/Trail_journal/ but under your own github), then click **sync** button. Fill in the token etc info to access your private data;
5. The trails record rely on GPX files (.GPX is a GPS data format). One way to obtain it is to export apple watch health data (you can easily find your workout routes in GPX format in the exported zip).


## Notes for myself or users who store their data under my github account:
Managing data for people who don't use github (their data will be hosted under my account)

1. Create private repo, say, named "data_tom". Then create fine-grained token to access this data repo (under Developer Settings -> Personal access tokens (Fine-grained tokens) -> Generate new token -> Token name, appropriate expiration time -> only selected repo -> select that private data repo for user -> Add permissions -> contents -> read and write -> done -> send that token to user)

2. On user side: after entering the app webpage -> Click Sync -> enter four pieces of info: my github user name (YuhengF), the private data repo (data_tom), the token I gave them, data file path (should be the same throught out the whole usage, default is data.json) -> optional encrytion (I won't be able to see their content at all after encrytion. User has to remember their passphrase otherwise they will forever lose access to their data).
