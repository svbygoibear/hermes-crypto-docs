---
marp: true
theme: custom-dracula
footer: "https://hermes-crypto.com"
header: <span><img src="./img/hermes-crypto-logo.svg" height="20px"/>  hermes-crypto </span>
pagination: true
---

# ☀️ Welcome

![bg right width:500px](./img/hermes-crypto-logo.svg)

Welcome to the `hermes-crypto` onboarding chat - ask questions and stop me at any time.

_[Simone van Buuren](https://github.com/svbygoibear)_

---

# Hermes?

![bg right :500px](./img/hermes-icon-image.png)

Who 'dis?

Hermes (called Mercury in Roman mythology) was considered the messenger of the Olympic gods.

---

<!-- Hermes (called Mercury in Roman mythology) was considered the messenger of the Olympic gods. He possesses the ability to influence outcomes and tip the scales in favor of those who seek his benevolence. As the god of luck, he brings both fortune and misfortune to those who dare to ask.

hermes-crypto is a fun page where you can ponder if the price of your coin will go up or down; place your bets, and see if the gods will be in your favour! -->

## What is hermes-crypto?

Hermes-Crypto is a fun, in-browser game with a greek theme that aims to be calming, non-competitive and whimsical. Users simply vote if the price of BTC will go up or down & we add or subtract to their score after 60 seconds; resolving the vote.

- `Goal`: Create a reliable page that is intuitive and fun.
- `Users`: For now? Technical folks.
- `Competitors`: Like us? Not many. All other pages dedicated to this up and running focusses on events and winning coins.

<!-- Give some more insight into the project itself:
How good are you at predicting whether the price of Bitcoin will go up or down in a given minute? Hermes-Crypto makes it possible for you to place your bet. It's simple: vote up if you think the price will increase within the next minute or vote down if you think the price will decrease within the next minute. If you guess correctly, you will get +1 point! Guess wrong... that'll be -1 on your total.

Once you've thrown down your speculation, you won't be able to vote for another 60 seconds. -->

---

### So what are the main features?

The game itself is simple; we want simple user identification & simple vote resolution coupled with clear feedback to users.

- Sign in > create user
- If not & you vote then > create dummy user
- We get the current BTC price in USD at vote
- Wait 60 seconds & check the latest BTC price at USD
- Update user score based on prediction

<!-- Mention here that the mechanism for determining the vote resolution can be improved but we will look at that later. -->

---

## 💣 Live Demo

> Don't tell me the moon is shining; show me the glint of light on broken glass. -_Unknown_

Let us look at [hermes-crypto.com](https://hermes-crypto.com)

<!-- Explain the flow of the page here. -->

---

### Assumptions

![bg right :500px](./img/hermes-landing-screenshot.png)

Vote state can be resolved, pending or expired. Expired votes are calculated as soon as the client checks for results.

Votes that are a draw, are currently counted towards `+1` point.

<!-- Again, mention that we can alter this, this was just left as a current assumption. -->

---

## 🔍 Tech Stack

We have 2 main `repos` to consider, those being:

1. [`hermes-crypto-core`](https://github.com/svbygoibear/hermes-crypto-core): B/E App in Go
   ![image height:100px](./img/hermes-crypto-core.png)
2. [`hermes-crypto`](https://github.com/svbygoibear/hermes-crypto): F/E using React & Typescript
   ![image height:100px](./img/hermes-crypto.png)

<!-- Mention for both VSCode has been used as development environments, but for setup on their machines they can use Goland or whichever IDE they feel more comfortable in. -->

---

## 📄 Backend Walkthrough

To cover the basics, we are working with:

- DynamoDB
- Golang
- Gin for routing

Time to look at what ticks under the hood!

You can have a look here: [hermes-crypto-core](https://github.com/svbygoibear/hermes-crypto-core)

<!-- Side-by-side demo of what currently exists in the B/E and its docs. -->

---

## 📄 Frontend Walkthrough

Overall the F/E consists of a page that makes use of:

- React & Vite
- Typescript
- And a few more bits and bobs...

Less talk, more show > let us head off to the code again.

You can have a look here: [hermes-crypto](https://github.com/svbygoibear/hermes-crypto)

<!-- Side-by-side demo of what currently exists in the F/E and its docs. -->

---

![bg opacity](https://picsum.photos/800/600?image=53)

## What is coming for the future?

| Feature          | Description                                                                    |
| ---------------- | ------------------------------------------------------------------------------ |
| Vote Review      | Re-look at our current method of calculating votes; async job to be considered |
| Add Logging      | Investigate and add better logging                                             |
| Improve login    | Add Oauth for better login & logout                                            |
| Create User Dash | Add a user dash with their stats and info                                      |

---

## Development Cycle

This is where you fit in. We've identified some opportunities, shortcomings, some enhancements that can be made and now; how do we tackle this as a team?

- Discuss in our morning meeting.
- Create issues; as part of our planning meeting we can discuss who grabs which features/issues.
- Create feature/bug branches.
- Code, commit & PR.

<!-- Explain these are procedures we should develop together and adapt as the need arises. Process should help us, not hinder us. -->

---

## Deployment

We already have automatic deployments, but what about adding our own staging environment to collaboratively review our work:

- Deploy after a successful Pull Request the code into staging & have an internal review phase/enhance testing
- After bundling a few staging items together, deploy them to production

<!-- Mention these are future plans. -->                                    |

---

## Open Discussion

Have more questions? Maybe some suggestions? Now is the time!
![bg right :500px](./img/player-won.gif)

---

# <!--fit--> END
