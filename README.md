I used claude to write this app to track my personal hiking record.
To use it on your own device, simply do the following:
1. Fork the repo (you can also use my existing github page session **https://yuhengf.github.io/Trail_journal/**, and all data files will be saved locally on your device);
2. Make sure it's public so you can enable Page function on github;
3. Create your own private data managing repo (say "my_data") on your own github, and then enable a fine-grained token to access this data;
4. Access the page hosting this trail journal html (using URL like **https://yuhengf.github.io/Trail_journal/**), then click **sync** button. Fill in the token etc info to access your private data;
5. The trails record rely on GPX files (.GPX is a GPS data format). One way to obtain it is to export apple watch health data (you can easily find your workout routes in GPX format in the exported zip).


### Notes for myself:
Managing data for people who don't use github (their data will be hosted under my account)
1.Create private repo, say, named "data_tom". Then create fine-grained token to access this data repo (under Developer Settings -> Personal access tokens (Fine-grained tokens) -> Generate new token -> Token name, appropriate expiration time -> only selected repo -> select that private data repo for user -> Add permissions -> contents -> read and write -> done -> send that token to user);
2. On user side: after entering the app webpage -> Click Sync -> enter four pieces of info: my github user name (YuhengF), the private data repo (data_tom), the token I gave them, data file path (should be the same throught out the whole usage, default is data.json) -> optional encrytion (I won't be able to see their content at all after encrytion. User has to remember their passphrase otherwise they will forever lose access to their data).
