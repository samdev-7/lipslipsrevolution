# LipsLips Revolution
> [!NOTE]  
> This fork is fixes the demo, as dependecies have changed

This was a group project for Hack the North 2024. The following description is copied from our [Devpost listing](https://devpost.com/software/lipslips-revolution). 

### [Demo Video](https://youtu.be/C_vZ8xYM-pw)

## Inspiration
Why not? We wanted to try something new. Lip reading and the Symphonic Labs API was something we hadn't seen before. **We wanted to see how far we could push it!**

## What it does
Like singing? LLR is for you! Don’t like singing? LLR IS STILL FOR YOU! Fight for the top position in a HackTheNorth lip-syncing challenge. How does it work? Very simple, very demure:

1. Choose a song. Harder songs -> more points.
2. Lip sync to a 10-15 second clip of the song. (Don’t mumble!)
3. LLR reads your lips to determine your skill of lip-syncing to popular songs!
4. Scan your HTN QR code to submit your score and watch as you rise in ranking.

## How we built it
LLR is a web app built with Next.js, enabling the rapid development of reactive apps with backend capability. The Symphonic API is at the core of LLR, powering the translation from lip movement to text. We’re using OpenAI’s embedding models to determine the lip sync’s accuracy/similarity and MongoDB as the database for score data.

## Challenges we ran into
While the Symphonic API is super cool, we found it slow sometimes. We found that a 10-second video took around 5 seconds to upload and 30 seconds to translate. This just wasn’t fast enough for users to get immediate feedback. We looked at Symphonic Lab’s demo of Mamo, and it was much faster. We delved deeper into Mamo’s network traffic, we found that it used a much faster web socket API. By figuring out the specifications of this newfound API, we lowered our latency from 30 seconds to 7 seconds with the same 10-second clip.

## Accomplishments that we're proud of
The friends we made along the way.

## What we learned
Over the course of this hackathon, we learned from workshops and our fellow hackers. We learned how to quickly create an adaptive front end from the RWD workshop and were taught how to use network inspection to reverse engineer API processes.

## What's next for LipsLips Revolution
We hope to integrate with the Spotify API or other music services to offer a larger variety of songs. We also wish to add a penalty system based on the amount of noise made. It is, after all, lip-syncing and not just singing. We do hope to turn this into a mobile app! It’ll be the next TikTok, trust…
