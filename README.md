# SharingShard

***
** Deploying contract **
***
Build contract:

`cargo build --target wasm32-unknown-unknown --release`

Use near-cli to deploy the smart contract to NEAR test network:

`near deploy --wasmFile target/wasm32-unknown-unknown/release/SharingShard.wasm --accountId <YOUR_ACCOUNT_HERE>`


***
** Initializing **
***

Initializing contract:

`near call <YOUR_ACCOUNT_HERE> new --accountId <YOUR_ACCOUNT_HERE>`

***
** Setters **
***

Add new user:

`near call <CONTRACT OWNER WALLET> new_user --args '{"wallet": "<USER WALLET>", "n": "<USER NAME>", "disc": "<USER DIRCORD>", "mail": "<USER EMAIL>", "interst": <CODE NUMBER FOR USER ITERESTS>}' --accountId <CALLER WALLET>`


Add new experience:

`near call <CONTRACT OWNER WALLET> add_experience --args '{"wallet": "<USER WALLET>", "experience_name": "<NAME>", "description": "<EXPERIENCE DESCRIPTION>", "url": "<VIDEO URL>", "reward": <MOMENT REWARD>, "expire_date": <EXPIRATION DATE>, "topic": <CODE NUMBER FOR TOPIC OF VIDEO>}' --accountId <CALLER WALLET>`


Add moment to experience:

`near call <CONTRACT OWNER WALLET> add_moment --args '{"wallet": "<USER WALLET>", "experience_number": "<CODE NUMBER FOR THE EXPERIENCE>", "time": <TIME ON THE VIDEO>, "comment": "<MOMENT COMMENT>"}' --accountId <CALLER WALLET>`

*************
** Getters **
*************

Get experience title:

`near call <CONTRACT OWNER WALLET> get_title --args '{"video_n": <EXPERIENCE NUMBER>}' --accountId <CALLER WALLET>`


Get experience description:

`near call <CONTRACT OWNER WALLET> get_description --args '{"video_n": <EXPERIENCE NUMBER>}' --accountId <CALLER WALLET>`


Get video url:

`near call <CONTRACT OWNER WALLET> get_url --args '{"video_n": <EXPERIENCE NUMBER>}' --accountId <CALLER WALLET>`


Get experience topic:

`near call <CONTRACT OWNER WALLET> get_topic --args '{"video_n": <EXPERIENCE NUMBER>}' --accountId <CALLER WALLET>`


Get experience reward:

`near call <CONTRACT OWNER WALLET> get_reward --args '{"video_n": <EXPERIENCE NUMBER>}' --accountId <CALLER WALLET>`


Get experience expiration date:

`near call <CONTRACT OWNER WALLET> get_expiration_date --args '{"video_n": <EXPERIENCE NUMBER>}' --accountId <CALLER WALLET>`


Get moment coment:

`near call <CONTRACT OWNER WALLET> get_moment_coment --args '{"video_n": <EXPERIENCE NUMBER>}' --accountId <CALLER WALLET>`


Get moment time:

`near call <CONTRACT OWNER WALLET> get_moment_time --args '{"video_n": <EXPERIENCE NUMBER>}' --accountId <CALLER WALLET>`


Get points of view for a moment:

`near call <CONTRACT OWNER WALLET> get_pov_of_vid --args '{"video_n": <EXPERIENCE NUMBER>}' --accountId <CALLER WALLET>`


Get experiences by topic :

`near call <CONTRACT OWNER WALLET> get_exp_by_topic --args '{"topic": <CODE NUMBER OF TOPIC>}' --accountId <CALLER WALLET>`


Get user's name:

`near call <CONTRACT OWNER WALLET> get_user_name --args '{"wallet": <USER WALLET>}' --accountId <CALLER WALLET>`


Get user's discord:

`near call <CONTRACT OWNER WALLET> get_user_discord --args '{"wallet": <USER WALLET>}' --accountId <CALLER WALLET>`


Get user's email:

`near call <CONTRACT OWNER WALLET> get_user_email --args '{"wallet": <USER WALLET>}' --accountId <CALLER WALLET>`


Get user's interests:

`near call <CONTRACT OWNER WALLET> get_user_interests --args '{"wallet": <USER WALLET>}' --accountId <CALLER WALLET>`


Get user's experiences:

`near call <CONTRACT OWNER WALLET> get_user_exp --args '{"wallet": <USER WALLET>}' --accountId <CALLER WALLET>`


Get experiences the user left a point of view:

`near call <CONTRACT OWNER WALLET> get_user_exp_pov --args '{"wallet": <USER WALLET>}' --accountId <CALLER WALLET>`


Get user's date of last comment:

`near call <CONTRACT OWNER WALLET> get_user_date --args '{"wallet": <USER WALLET>}' --accountId <CALLER WALLET>`


Get total of experiences in the contract:

`near call <CONTRACT OWNER WALLET> get_number_of_experiences --accountId <CALLER WALLET>`
