---
marp: true
theme: custom-dracula
footer: "https://hermes-crypto.com"
header: <span><img src="./img/hermes-crypto-logo.svg" height="20px"/>  hermes-crypto </span>
pagination: true
---

# ☀️ Welcome

![bg right width:500px](./img/hermes-crypto-logo.svg)

First day? Lost?

Lets get started on the right foot!

Welcome to your onboarding chat - ask questions and stop me at any time.

---

<!-- Speaker Notes -->

## What is hermes-crypto?

We are a fun, in browser game with a greek theme that aims to be calming, non competitive and embodies being whimsical. Users simply vote if the price of BTC will go up or down & we add or subtract to their score after 60 seconds; resolving the vote.

- `Goal`: Create a reliable page that is intuitive and fun.
- `Users`: For now? Technical folks.
- `Competitors`: Like us? Not many. All other pages dedicated to this up and running focusses on events and winning coins.

<!-- Give some more insight into the project itself -->

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

### Assumptions

![bg right :500px](./img/hermes-landing-screenshot.png)

Vote state can be resolved, pending or expired. Expired votes are calculated as soon as the client check for results.

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

## 💣 Live Demo

> Don't tell me the moon is shining; show me the glint of light on broken glass.

What use will it be to just talk about what is going on under the hood and not show what we are actually working with? Time to hop on off to [hermes-crypto.com](https://www.hermes-crypto.com)

![image height:200px](./img/hermes-landing-screenshot.png)

---

## Slide 4

| Column 1 | Column 2 |
| -------- | -------- |
| Item 1   | Item 2   |
| Item 3   | Item 4   |

---

![bg opacity](https://picsum.photos/800/600?image=53)

## Slide 5

<div class="columns">
<div>

## Left

- 1
- 2

</div>
<div>

## Right

- 3
- 4

</div>
</div>

---

## Slide 6

<i class="fa-brands fa-twitter"></i> Twitter:
<i class="fa-brands fa-mastodon"></i> Mastodon:
<i class="fa-brands fa-linkedin"></i> LinkedIn:
<i class="fa fa-window-maximize"></i> Blog:
<i class="fa-brands fa-github"></i> GitHub:

---

# <!--fit--> Large Text

---

<!-- Needed for mermaid, can be anywhere in file except frontmatter -->
<script type="module">
  import mermaid from 'https://cdn.jsdelivr.net/npm/mermaid@10/dist/mermaid.esm.min.mjs';
  mermaid.initialize({ startOnLoad: true });
</script>

# Mermaid

<div class="mermaid">
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
</div>
