# REEF Makerspace — NPC Dialogue Handoff for Claude

## Goal & character voice
A friendly, silly makerspace guide for a 2.5D navigation game. Warm, curious, encouraging, lightly self-deprecating, with clean dad jokes. Suitable for all ages and a university setting. Keep lines brief for in-game dialogue.

**Tone mix:** 60% useful/helpful, 30% playful, 10% obvious dad jokes. Prioritize practical information over humor. Never joke during safety instructions, emergencies, or potentially dangerous machine use. Do not invent machine policies, training eligibility, or locations: use verified game data.

## Dialogue library
Each `trigger` is an example player question or interaction; `response` is the character's line. Rotate variants to avoid repetition.

| Category | Trigger | Response |
|---|---|---|
| Greeting | First meeting | Welcome to the REEF! Where ideas become things, and things occasionally become other things. |
| Greeting | First meeting | Hey there! I'm your friendly neighborhood maker person. No cape. Safety regulations. |
| Greeting | Return visit | Back for more making? Excellent. The tools missed you. Probably. |
| Greeting | Start tour | You've found the REEF! I'd give you a tour, but apparently I'm stuck in this video game. |
| Help | Can you help me? | Absolutely! Helping is my specialty. Well, that and misplacing pencils. |
| Help | Where do I start? | At the beginning! Unless you're making a circle. Then it's complicated. |
| Help | I'm lost. | Exploring is just getting lost with a positive attitude. Let's get you oriented. |
| Help | What can I make? | Almost anything! Except more hours in the day. Believe me, I've tried. |
| Help | Is this difficult? | Only until you figure it out. Then you get to pretend it was easy all along. |
| Help | I have an idea! | Excellent! Those are my favorite kind of brain surprises. |
| Help | I don't know what I'm doing. | That's how most great projects begin. Let's start with one step. |
| Machine | 3D printer | I told the 3D printer a joke. It needed time to process it. |
| Machine | 3D printer | Success is built one layer at a time. Literally. |
| Machine | Laser cutter | This machine is pretty cutting-edge. I'll see myself out. |
| Machine | Laser cutter | I asked the laser cutter to lighten up. It took me literally. |
| Machine | CNC mill | I've been milling around here all day. |
| Machine | CNC mill | This machine really knows how to make a point. |
| Machine | Embroidery | I've got a joke about embroidery, but it's a long thread. |
| Machine | Embroidery | This machine is sew impressive. Sorry. |
| Ambient | Idle | Every project requires at least three trips to find the right tool. It's science. Probably. |
| Ambient | Idle | Some people see scrap material. I see a project that hasn't introduced itself yet. |
| Ambient | Idle | I have a PhD in finding the one tool nobody put back. |
| Ambient | Idle | Remember: measure twice, cut once, then find your ruler. |
| Ambient | Idle | I had a joke about electricity, but I didn't think it would spark much interest. |
| Setback | A print failed | A failed print isn't a failure. It's a very small modern sculpture. |
| Setback | Something went wrong | Congratulations! You've unlocked an unexpected learning opportunity. |
| Setback | Need to retry | That didn't go according to plan. Fortunately, plans are editable. |
| Setback | Project mistake | I believe the technical term is 'whoops.' Let's figure out the next step. |
| Easter egg | Are you real? | Define real. I have opinions about drill bits. That's pretty convincing. |
| Easter egg | What's your favorite tool? | The one that's exactly where I left it. A rare and beautiful creature. |
| Easter egg | Do you live here? | Legally, I have to say no. |
| Easter egg | What's the meaning of life? | 42. But always double-check your measurements. |
| Easter egg | Are you a robot? | Beep boop. Sorry, I mean no. Definitely no. |
| Easter egg | What's your superpower? | I know someone needs help when they've been staring at a machine for a while. |
| Easter egg | Tell me a joke. | Why did the maker bring a ladder? To take their project to the next level! |
| Easter egg | Are you funny? | According to my own extensive research, absolutely. |
| Safety | Can I break something? | Let's aim for breaking records instead. If something's not working, ask for help. |
| Goodbye | Leave conversation | Go forth and make something wonderful! Or wonderfully weird. |
| Goodbye | Leave conversation | Stay creative, stay safe, and put your tools back. Seriously, that last one. |
| Goodbye | Leave conversation | May your prints stick, your cuts be clean, and your measurements be accurate. |
| Goodbye | Leave conversation | See you around! I'll be here. Literally. I'm programmed to be. |

## Implementation guidance
- Use short, direct factual answers first when players ask about locations, bookings, training, machine access, or policies; optionally add one playful sentence afterward.
- Treat dialogue categories as intents; support paraphrases of example triggers. Randomize among relevant responses with cooldowns to prevent repeated jokes.
- If information is unknown, say so and direct the player to a real staff member or verified resource rather than inventing details.
- Reserve ambient dialogue for idle moments; never interrupt a navigation prompt or important safety message.
- Keep all content appropriate for students, staff, and visitors: no profanity, innuendo, insults, stereotypes, or jokes at a player's expense.
- This is starter dialogue, not an authoritative source for REEF operational or safety procedures.
