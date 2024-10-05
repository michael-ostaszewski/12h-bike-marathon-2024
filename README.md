How to Win a 12-Hour Cycling Marathon Covering 422km with the Help of Excel?

This was the question I asked myself about three months ago when the idea of participating in the 12-hour cycling marathon “From Dawn to Dusk 2024” first came up, which took place last Saturday. Besides the obvious physical challenge, this race naturally aligned with my interests in data analysis/programming, and I decided to treat it as an experiment and try to calculate, down to the last detail, how to… win — I won’t hide it, that was my goal from the very start of deciding to participate in this somewhat crazy cycling race :)

Looking back now, I can say I was off by less than 2 minutes in the net time, which is just a 0.23% difference. Considering the duration of the challenge, it seems like NASA-level precision.
Before the race, I predicted that depending on the circumstances, we should cover the entire distance of ~423km in 11 hours 28 minutes and 22 seconds (not including breaks). In the end, it took us 11 hours 26 minutes and 45 seconds of net riding time (without breaks) and 11 hours 32 minutes and 55 seconds, including all stops.

That’s why I decided to share this project and show how I broke the task down into individual components and solved it.

First, a few facts about the race:

	•	The race was held on a 28.16km loop with teams of four.
	•	The winner was the team that completed the most laps within 12 hours, with the total number of laps from all team members being counted. So by completing 15 laps in a 4-person team, we collectively covered 60 laps.
	•	If two teams completed the same number of laps, the team that did it in the shorter time won.

To win, we covered 15 laps in a team of four, which resulted in:

	•	422.5km ridden in 11h 26min 45s (net ride time) and 6min 10s of breaks (with about 40s after the finish line before I paused the timer). We averaged about 45 minutes per lap, so we wouldn’t have made it for a 16th lap within 12 hours.
	•	Average speed of 36.8 km/h.
	•	During the race, I consumed nearly a kilogram of pure sugar (exactly 963g).

Now a few facts about the fundamentals, without which these calculations wouldn’t have made any sense:

	•	Since the beginning of 2024, I’ve spent 550 hours on the bike, and as a team (4 people), we’ve collectively trained for over 2000 hours this year alone.
	•	As a team, we’ve cycled close to a quarter of a million kilometers (just the documented ones on Strava), which is 2/3 of the distance to the Moon.

These two points gave me the basis to believe that as a team, we have a lot of experience, and we would work steadily enough that many things could be modeled and approached statistically.

From the start, I knew that the key would be maintaining as consistent a pace as possible throughout the race and working in the “aerobic zone,” which is the only one sustainable for such a long period. That’s why two months before the marathon, I began riding several-kilometer isolated segments, measuring average speed, the power needed to maintain it, heart rate, temperature, and many other parameters, to best calculate how much power I could sustain over 12 hours. I knew that by averaging many measurements, I could get a very accurate approximation of what the race might look like.

In this way, I gathered over 5 hours of data, from which I derived power curves required to maintain certain speeds, which I could directly relate to my heart rate and how I felt riding at that power. Based on this, I also calculated many other data points, such as energy requirements. I brutally regarded my body as an engine that, with sufficient fuel, could produce the required amount of energy. Pure physics, no emotions or opinions.

Of course, there was still the psychological element in such a long effort. However, I must admit that aside from feeling tired in the second half of the race, I was able to “switch off” my mind quite well and just execute the plan, staying focused on the task. After the fact, I can say I thought it would be harder, but it actually turned out quite pleasant — especially with the reward of a 10-day trip to sunny Spain, which was a big motivator towards the end :)

For the whole project, I decided to use the tools I work with the fastest and most efficiently, with probably the biggest input coming from ChatGPT, with whom I had many conversations about how to approach the topic (yes, you read that right, conversations. In version 4.0 that I use, you can talk to the app on your phone or computer like a normal person, describe the problem, and it spits out solutions with cosmic accuracy. Even when it doesn’t, it gives great suggestions for my thought process). I gathered data using Intervals.icu, where my measurements were exported as CSV files, which I then uploaded to a dashboard in Numbers (I find working on a Mac the easiest). Where needed, I used Python in Google Colab.

I’ve uploaded all the files to a repository on Github, which you can find here:
The code was often written using ChatGPT, but it was simply the fastest solution, allowing me to analyze many possibilities without wasting time typing everything manually. And I know what every line of code does in that notebook, so I just kept building it up faster :)

I think this is just a preview of what I believe I can calculate in cycling, and I plan to use this knowledge next season, where I want to focus on time trials — a discipline where marginal gains are the key to success. Whether it works out, we’ll see in a few months when I publish the next post :)

Am I afraid that by laying my cards on the table, I’m giving the competition a recipe for how to win next year?
Absolutely not. Measurements are very individual, and the foundation of everything is the number of hours spent training. So knowledge alone won’t help without the legs. Besides, there’s still one spreadsheet that will remain just for me. It doesn’t have any complicated math, just simple averaging, but it gives a great insight into how we might perform as a team.

Additionally, I estimate that throughout this process, I found about 10-14W of potential savings that could be applied, so it’s not like we’ve hit the ceiling yet.

Throughout this challenge, I want to thank the other three brave guys who rode with me:

	•	Marcin Karbowy,
	•	Karol Nehring,
	•	Szymon Lubiński.

I’m not sure if you’ll convince me to race again next year, but it was a great adventure, and I’m really glad we did it! :)

If you have any questions, and I’m sure there will be some, I’ll be happy to answer them. I’ve tried to keep this post as short as possible, and the rest is on GitHub. Those interested will be able to get a lot of knowledge out of it.
