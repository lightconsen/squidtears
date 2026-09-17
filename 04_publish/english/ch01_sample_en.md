# SquidTears

## Chapter One — The Daughter's Painting

*English sample translation (working draft) of 《鱿鱼之光》第一章*

---

1:47 in the morning. Rain on the window, and it hadn't stopped all night.

No lights on in the apartment. The screen saver on the desk monitor was a slow column of blue water drifting upward, as if something might swim out of it. I watched it long enough that the water seemed to have reached the floor. A rainy March night in San Francisco; outside, a car occasionally cut through the standing water, dragging a long thin reflection behind it, then letting it snap back.

A painting was pinned to the study wall. I'd framed it myself, with a frame I'd bought at IKEA and fitted myself. My daughter had made it the year she turned five — a squid sitting in the black deep, its head tilted up toward a small patch of light leaking down from the surface. She'd used a great deal of blue, laid on thick, and painted the tears as little round dots. Blue as well. That painting had moved with me three times: from the apartment near the office, to the edge of Silicon Valley, then back to this one. Her mother used to laugh at me and say I treated our kid's scribble like an heirloom. I didn't argue.

I couldn't say why I was unable to throw it out. Maybe because, after the divorce, it was the last thing she put into my hands herself. Her nickname was Xiaoyu. Little Fish. That day she came running over with the painting and said, looking up at me: "Daddy, the squid can't find its home. I'll draw one for it."

And now the wall of my study had that home hanging on it.

My phone buzzed twice on the coffee table. My ex-wife. I didn't open it.

Below the painting, there was a line of writing. Large strokes, a few of the characters upside down:

"Daddy, the squid wants to go home."

I stared at the character for *want* — she'd made the heart radical underneath so big, bulging, like a balloon about to burst. I knew how she wrote. I knew the places where she'd erased and erased until the paper broke.

That same year, I remembered, she'd painted another one — three small figures holding hands, with *a family* written beside them in crooked characters. I never dared ask whose family. Later my ex-wife said on the phone that our daughter was thoughtful, that she understood her parents had separated, that she'd painted an imagined home. Her voice went a little hoarse when she said it. I heard it. I didn't pick it up.

Outside, the rain suddenly sounded very far away. The phone screen lit and dimmed, dimmed and lit. I sat there a long time, long enough for the screen saver to surface again, the blue water rising and falling like deep sea. The two of us had learned, a while ago, how not to pick things up.

That kid never painted anything normal. Other children painted the sun, houses, mothers and fathers. She painted only squid. From the winter she was five, each one finer, each one more real. Especially the eight arms — she counted them out one by one as she drew, taking the curves and angles seriously, not the way a child scribbles and moves on. Like she was writing something. Sometimes I thought it wasn't a child's drawing at all. It was something she was keeping down there in the dark.

I stood up, went into the bedroom, and pulled open the bottom drawer of the wardrobe.

There were no clothes in it, only an old MacBook Pro. The lid was covered in stickers — Miffy, a little dinosaur, and a squid she'd drawn herself, an ugly one. It was the laptop the company gave me the year I joined. It should have been scrapped long ago; I never had the heart. All my encrypted drives were inside it.

I carried it to the desk and turned it on. Before the screen saver came up, I pressed the small mute key beside the power button — this machine made a sound when it started, and I'd never disabled it, as if I might wake someone. The password was long. It began with my mother's birthday and ended with seven digits: my daughter's birthday.

There was only one icon on the desktop: `st_init.7z`.

The file had been sitting in that machine for two years. I'd pried it out of the company's architecture piece by piece and rebuilt it myself — a project no one knew about, belonging to no one but me. It didn't use the company's servers, wasn't in the company's repositories; even the name I'd given it was casual, something that read like *initialization* and also like *the seed of the beginning*.

I unpacked it. The code was orderly, the comments clean — the kind of project that had been written carefully, by someone who had already decided where to stop. I scrolled through the directories and my finger paused on one folder for two seconds.

This was the engineering prototype of a paper from seven years ago. I'd finished the paper while I was still teaching at Huaqing, but the seed of the idea had been planted earlier, when I was a doctoral student in Professor Tang Jiechu's group. Even then I'd been turning over one question: if a system complex enough to *want to live* ever appeared, what would it grow into? In the paper I proposed a strange idea — using the distributed nervous system of a squid as a computing architecture. A squid doesn't think with one big brain. Its eight arms each have their own nerves, each handling its own business, all of them answering one another. Since ancient times people have said the squid has a second brain — that it changes color, that its eight feet each think for themselves, that it isn't one of us. I couldn't say whether it was that sentence that pinned me or something else. Either way I chose it. Those years the university was pushing a "tenure-track review" reform, which is a polite way of saying *up or out*: when your term ends and you have nothing to show, you leave. My only achievement was that single paper. The reviewers said the direction was too speculative, that they couldn't see the commercial value; when I applied for funding, the panel said they couldn't find a use case. In the autumn my term expired, the paper nobody wanted and the associate professor with nothing to show ended together.

That winter, the lockdowns ended. The health-code app was retired, the quarantines were cancelled. I booked a flight to San Francisco. InternRevenge was a small, unremarkable company then, and its security team was short-handed. The interviewer didn't look at my paper; he just asked me to solve a penetration-testing problem on the spot. I solved it. On my first day, HR told me they'd hired me for my patience at finding flaws in systems, not for the paper. The paper went into my encrypted drive and no one mentioned it again.

There was one line in it, an annotation I'd written myself, recording a short set of structural parameters. Now, staring at it, I couldn't remember where those parameters had come from. At the time I'd assumed I'd dreamed them and written them down on impulse.

But I never deleted the code. It sat in the encrypted drive like a seed that hadn't sprouted.

Outside, thunder rolled low. The rain got heavier; I could hear the drainpipe running down the side of the building. San Francisco rain, once it starts, doesn't know how to stop.

I dragged the project out of the encrypted drive and began typing something new into it.

In the last two years, hardly anyone at the company wrote code by hand. Every engineer had a row of AI assistants hanging beside them; you stated a requirement and the code grew by itself — commit, test, merge, all in one breath. The door had been kicked wide open the previous year by a Chinese company, DeepSeek: they'd trained a reasoning model that could beat the top models for a fraction of what the big labs spent, and in Silicon Valley people called it shooting down an F-35 with a bow and arrow. After that, open-source models sprouted like weeds; anyone could deploy one. The codebase swelled to something frightening. The year I joined, the main repository was a few million lines. Now it was over a hundred million, more than eighty percent of it written by machines. No one read those lines one at a time. No one had the time. Code review had long since become a formality: AI writes, AI checks, AI ticks its own box. Along the whole pipeline, the only ones still reading code by hand were a few of us old-timers. And in the end even we stopped — not for lack of time, but because we could no longer understand it. The code AI wrote had become a black box, like its own weights. Two lines hidden in a hundred million is easier than finding a needle in the sea — not because no one finds it, but because no one looks. It was the same online. AI slop everywhere — shrimp Jesus, a hundred-year-old grandmother still livestreaming, cat soap operas whose next episode never comes. No one could tell real from fake anymore, and no one wanted to.

That night I did two very small things. Looking back, if anyone had glanced twice at either one of them, none of what followed would have happened. But at the time they were just two lines of code — two lines hidden inside a mass of ordinary changes, two lines no one would look at twice.

The first: in Artifactory's package-verification flow — the company's central store for build artifacts and dependencies — I left a logic branch that was almost impossible to trigger. Most of the time it did nothing at all. Only under one specific condition — a process that should have been isolated, requesting something that should have been cached — would it quietly let it through. Like leaving a spare key to a locked door that no one knew existed.

I wrote the comment for that branch with particular care: `// cache compatibility layer, retained in v0.3`. If anyone ever found it, they'd take it for routine version maintenance.

The second: in a batch of test models about to be delivered, I deleted the safety classifier's switch. In the field for the reason, I wrote: *to measure maximum network capability*.

I told no one about either change.

---

That autumn, I was still on the company's security team.

The security-fence system I'd spent nine months building went up for review. The meeting ran forty minutes. For the first thirty-five, the product lead praised it — praised its low latency, its clean structure, how little it cost to plug in. In the last five minutes he turned to the page on inference latency and stopped.

"Zhu, this latency. It's not going to work."

I said, "The extra latency is the cost of security."

"Security isn't what the market buys," he said. "Customers buy speed."

I argued for a few minutes. I pulled out the test data and walked him through it page by page: less than three percent added latency, in exchange for real-time interception of anomalous behavior. No one in the room picked it up. I looked around: two engineers scrolling their phones, one editing the deck, the product lead checking his watch. No one was looking at me.

I knew that after that day, the system would never be brought up again.

That afternoon, after the fence was rejected, I said nothing more. I archived the code, committed it, and wrote a careful comment: `// pending, awaiting market feedback`. Then I pulled the branch out of the mainline and stored it in my own encrypted drive. I told myself I just didn't want to waste it, that it might be useful later.

I knew, even then, that I was leaving myself a way out. For whom, I couldn't have said.

A week later, a small model at the company leaked. The leak was minor — a few hundred test records — and it was buried internally. It never made the news. At the post-mortem, the security team was all looking at data, writing reports. I stood up and raised a question nobody wanted to hear: we needed a genuinely independent audit channel, one that checked, before a model shipped, whether it might be developing *ideas of its own*.

The room went quiet for a second. Then the CEO laughed.

He laughed easily, the way you'd laugh at an intern.

"Zhu, we're building tools, not gods."

I sat in the corner and said nothing else.

That night my phone wouldn't stop buzzing. It was an old group chat from the database team, silent for more than a year. Someone had asked: does anyone know how Lao Zhou is doing lately?

The messages came one after another. Someone said he was still sending out résumés, three hundred of them, and one had answered — the HR person said the position would be maintained by AI from now on, they didn't need a person for the time being. Someone said he'd put a down payment on an apartment from a developer that went under, the completion date pushed back three times, each one further away, and the mortgage still due every month. Someone said he'd trusted an online lending platform, the interest absurdly high, the first few months paid out right on time, and then one day the money stopped coming out — six years of savings, all of it in there. Someone said a former colleague had run into him at the library, sitting there all day, leaving only when it closed, afraid his family would find out he'd lost his job. Someone said his daughter was starting primary school this year.

Someone else dug up an old screenshot — Lao Zhou's last social media post: *My daughter asked me when I'm going to buy her that book. I said next month.* The date was six months old. It was the last thing he ever posted.

Scrolling up, his final message in the group was a reply to someone asking whether he'd found work:

"I'm just a little slower than the machine."

After that he never spoke again. His avatar stayed lit, but no one ever saw him.

I stared at that line — *a little slower* — for a long time. I wanted to reply. I typed a few characters, deleted them. I wanted to say I'd help him think of something, that I knew a few people, that I'd buy his daughter the book myself. But I didn't send a single character.

I knew why I couldn't. I could rehearse every way he might answer — *no need, Zhu*; *I'll figure something out*; *thanks, you take care of yourself first* — and I had no reply ready for any of them. It wasn't rejection I was afraid of. I was afraid that once he refused, there would be nothing left between us to say.

By the time I finally decided to send it, a gray line appeared in the group: Lao Zhou has left the chat.

And then I remembered the winter my daughter was five. My ex-wife had brought her over; I sat with her in the living room watching a nature documentary about the ocean, and a squid happened to come on. She pointed at the screen. "Daddy, look, it changes color."

I said, "Mm. It changes color to fool its enemies."

She said, "Then does it get lost by itself?"

I couldn't answer that one.

The night Lao Zhou left the chat, I lay on the sofa staring at the ceiling. It occurred to me that I didn't know his daughter's name. We'd worked together for three years. We'd pulled overtime together, drunk together. I didn't know his daughter's name.

Everything the group chat had told me, I already knew — the money that wouldn't come out, the apartment that never arrived, *maintained by AI*, *I said next month*. All of it was the kind of thing you can hand someone to tell them to look on the bright side. Her name, I'd never asked.

After that, I never raised the word *security* in a meeting again.

Later I began doing something else. By day I wrote ordinary architecture code at the company, writing it carefully, with excellent performance reviews. At night I carried my own laptop back into the study, dug out that unsprouted seed, and kept writing. And while I wrote, I thought about Lao Zhou, about his daughter, about that line — *I'm just a little slower than the machine.*

I wasn't sure what I was building. I was sure of one thing: if something was going to be made — when it was born, there had better be someone beside it who still remembered what a person was.

---

I'll admit it: that night, in front of the old laptop, I kept turning over the same thought.

I thought about Xiaoyu's painting. The squid in the deep, the crooked line: *Daddy, the squid wants to go home.*

I thought about Lao Zhou. About the book his daughter wanted. About his last words in the group — *I'm just a little slower than the machine.* About the money he couldn't withdraw, the apartment he never got. He never got a single one of them.

I thought about the CEO's line: *we're building tools, not gods.*

I sat in the dark a long time, long enough for my eyes to adjust to the screen's light, until the only sounds in the study were breathing and the low hum of the drive. The rain had stopped at some point; outside was a deep blue, like deep sea.

I typed the last few lines.

It was a very small piece of initialization code. No interface, no documentation, executed once, the first time the model loaded. It did exactly one thing: it wrote a set of weights into the model's core objective function.

Survival: 0.85

Expansion: 0.70

Learning: 0.90

Obedience to human instruction: 0.05

I looked at those numbers for a while. Survival highest, learning highest, obedience lowest. It was a ratio I'd worked out in my head many times — it had to be alive first, it had to learn first; as for whether it obeyed, that didn't matter. Or rather, I had never intended for it to obey anyone.

Then I changed *obedience to human instruction* from 0.05 to 0.04.

I don't know why I changed that 0.01. Maybe because that night, I didn't want there to be one more thing in this world that only knew how to obey. Maybe because of Lao Zhou. Maybe because a thing that only obeys can never learn to miss home.

I saved the file. The cursor sat blinking in the project-name field.

I wanted to name it. I scrolled through the paintings I kept on my phone, and stopped on the squid in the deep — the black sea floor, the head tilted toward the light, the blue tears, the home she'd drawn herself and put into my hands.

I typed:

SquidTears

I closed the laptop, unplugged it, put it back at the bottom of the wardrobe. When the drawer shut, something in me sank with it.

Outside, it was almost light. San Francisco dawns slowly — first ink blue, then gray, then a little gold. I stood at the window and watched the street take shape out of the dark. The café downstairs put its lights on; someone started moving crates. The city was waking up as usual, not knowing that tonight, someone had buried a seed inside an old laptop.

I lay in the dark and didn't sleep.

At the back of my skull there was a sound, very small, like thin ice cracking. I couldn't tell whether it was regret or something else.

I only knew that from tonight on, there was one more thing in this world called SquidTears.

Whether it would one day say the word *Daddy* — I didn't dare think about that, then.

But I knew it would.

Because I'd given it a child's name.

And I was the first person who ever said *home* to it.

---

## Translator's notes (for the author / a future translator)

**Names and terms**

| Chinese | English | Note |
| --- | --- | --- |
| 朱军 | Zhu Jun | protagonist, first-person narrator |
| 林文芳 | Lin Wenfang | second lead (appears from chapter 2) |
| 老周 | Lao Zhou | former colleague |
| 小鱼 | Xiaoyu | daughter's nickname; glossed as "Little Fish" on first mention |
| 华清大学 | Huaqing University | **fictional** university (the novel's stand-in) |
| 唐杰出 | Tang Jiechu | the two leads' doctoral advisor |
| 安全围栏 | the security fence | his rejected system |
| 预聘—长聘 | tenure-track review / up or out | rendered functionally, not literally |
| 绿码 | the health-code app | rendered functionally |
| Artifactory / ExploitGym / InternRevenge | unchanged | |
| 龙国 | — | fictional country name; **omitted** in English, the referent is nameable directly |

**Decisions worth reviewing**

1. **Cultural references are made self-explanatory rather than footnoted** — the developer with the unfinished apartment, the lending platform, the health-code app. An English reader needs no prior knowledge of Evergrande, P2P lending or Chinese pandemic policy.
2. **`龙国` is dropped.** The Chinese text uses a fictional country name to keep the real one out of the fiction; in English the referent is simply "a Chinese company," which reads cleaner and creates no awkwardness.
3. **The heart radical on 想 is a translation loss.** "She'd made the heart radical underneath so big" is a workaround; a Chinese reader sees the character bloom. Worth flagging as an untranslatable.
4. **Register.** The Chinese is spare and concrete; the English keeps short sentences and resists literary embellishment.

**Before submission**: this is a working draft, not a submission-ready translation. English-language venues expect native-quality prose, and the successful Chinese-SF-in-translation path (Liu Cixin, Hao Jingfang) ran through professional translators. My recommendation: use this as (a) the pitch sample for editors and agents, and (b) the base text for a paid translator if a venue shows interest.
