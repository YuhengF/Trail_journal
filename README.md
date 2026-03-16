I used claude to write this app to track my personal hiking record. I tried to include all functionalities I feel excited about (especially those not included by popular hiking apps, for example showing all past trails altogether on the map, which gives people sometimes sense of achievements as if they're wandering in their kindom of hiking realm). Bugs might exist, please feel free to leave a message for any comments or suggestions. 

## To use this app

### If you don't want to touch any programming work:

1. You can use my existing github page session **https://yuhengf.github.io/Trail_journal/**. In order to sync your data, you need to contact me to create a private data repo for you under my github account. If you don't enable Sync you can still use the app but then all data files will be saved locally on a single device (you can export the json and import it on other devices but it's a bit of hassle);
2. To establish Sync, in your first time usage (or on a new device): visit the app webpage **https://yuhengf.github.io/Trail_journal/** -> Click Sync (bottom left) -> enter four pieces of info: my github user name (YuhengF), the private data repo (I will tell you what is, something like "data_tom"), the token I give you (will be a very long string), data file path (default is data.json which is good; you can also name it your own way if you understand what .json kinda means, and it should be the same throught out the whole usage across devices) -> optional encrytion (**I won't be able to see your content at all after encrytion. User has to remember their passphrase otherwise they will forever lose access to their data**). You need to fill the same information again everytime you want to use it on a new device;
3. To create new trails you can either draw on the map (this is an exciting tiny functionality I like about my app), or you need .GPX files (.GPX is a GPS data format). One way to obtain .GPX is to export apple watch health data (you can easily find your workout routes in .GPX format in the exported zip).


### If you want to do everything yourself:

1. (Optional) Fork the repo. Make sure it's set to public so you can enable **Page** function on github;
2. Create your own private data managing repo (say "my_data") on your own github (note this page can be hosted on my github while you own your own data repo)(slightly more tech details: you can "use" my Page but store data elsewhere is because it's a pure frontend setup, and the rendering work is done on your browser, and there's no server/backend behind this Page app on my side). And then enable a fine-grained token to access this my_data repo;
3. In the first time setup of the app, access the page hosting this trail journal html (would be something like https://yuhengf.github.io/Trail_journal/ but under your own github), and then click **sync** button. Fill in the token etc info to access your private data;
4. The trails data rely on GPX files (.GPX is a GPS data format). One way to obtain it is to export apple watch health data (you can easily find your workout routes in GPX format in the exported zip).

## Why I save the data in this way:
Just so I don't need any server or datasync services other than github. There're a million of other ways, but this way is the most viable if someone wants to deploy this app when they have and only have a github account.


## A fun metaphor of this whole thing (app/data/encryption/etc) I thought of and might help you understand intuitively:
1. Github is like a hotpot restaurant that has lots of tables with lots of hotpot machines
2. I am one of their customers who currently sits at and rents/uses one of thier hotpot matchines (=my github account)
3. I use the hotpot machine (=my github account) to make some tasty hotpot soup (=this web app I design and make)
4. Other customers in the restaurant (=other github users) are welcome to grab some of my soup/recipe (=my web app) to their own table/hotpot machine (=their own github accounts)
5. Because the restaurant is open and I as well welcome you to come to use it even if you don't currently have your own table/hotpot machine in the restaurant (=your own github account)
6. When you come over thinking about to use my customized soup to cook some food, you take out your own chopsticks (=your device like phone/laptop and the browsers on them), and you grab some raw food material you bring (=your data and your hiking/running record/experience) using the chopsticks (=your device)
7. Now using my soup (=this web page app) and with your chopsticks (=your device) you've made some tasty cooked food, say some meat balls (=organized/processed data or the trail record my app produced for you)
8. You can pass your meat ball from one pair of chopsticks (=your first device) to another pair (=your second device), but there're cases when you need to head out and come back later but you don't want to take your meat ball with you all the time (you can if you want!), or it could be that you have too many meatballs and your chopsticks cannot hold all of them (=you generate too much data and your device cannot store them)
9. Now I tell you, I have a food box I rent from the restaurant (=the "github data repository" I created) for you to put your tasty meat balls in (=to store your processed data in). And because there's some magic on the food box, only I, you and other granted friends can use it (the grant here means the token I generate and give you to sync your data, and *magic* food box = *private* github data repository)
10. Now you are happy and you can transfer your meat balls (=your processed/organized data) from your chopsticks (=your own device and browser) to the magic food box (=private data repository I currently own). Whenever you want, you can come back and use any pair of your chopsticks (=any of your devices) to take those meat balls out (=using any device of yours to reaccess your trail journal)
11. Instead of letting other friends of mine to use the same magic food box with you, I can also grab another magic food box for them (=create another private github data repo for them) so that you both dont need to worry the other person can access your own private meat balls
12. However other people who drop by can bring their own magic food box (=their own private github data repository) and put their meat balls cooked in my soup in their own box (and as mentioned before, they are welcome to just grab some of my soup to their own hotpot machine without using mine!), so that neither I or you can access those meat balls
14. In some cases you might think "I don't want other magic food box granted users to also touch my meat balls!" so you ask me and I encourage you to put a lock (=data encryption) on the magic food box. Then even I cannot open up the box. On the other hand if you forget your key to the lock (=foret the passphrase when you establish the encryption) you will never be able to take out and appreciate your tasty meat balls! I wish but I cannot do that for you!

(You're welcome to think of the metaphors of other more advanced operations, for example if I store your data directly in a public json file together with the Page session? Or if someone wants to use other cloud services or data servers?)

## Notes for myself or users who want to know techinically/procedurally how I store their data under my github account:

1. Create private repo, say, named "data_tom". Then create fine-grained token to access this data repo (under Developer Settings -> Personal access tokens (Fine-grained tokens) -> Generate new token -> Token name, appropriate expiration time -> only selected repo -> select that private data repo for user -> Add permissions -> contents -> read and write -> done -> send that token to user);

