## Day 10 of 365. Discipline, planning, anxiety.

10 days since the first post, wow, I managed to achieve so little of what is really important. But I needed a little rest and time to do some chores and errands, time to see friends and gather my thoughts.

I joined the YC startup school, not planning to apply to YC, but definitely useful to learn all the things they have to offer. Plus, using their weekly reporting tool as someone kindly suggested in comments. We'll see where this goes.

### a lifecycle

I was focused on getting some kind of routine for myself to be energetic and productive. It was rarely the case in my past life - I'd always find a way to live a spontaneous life schedule while still managing to put **a lot** of work hours irregularly distributed over a week.

But I want this time to be different. I feel like I'm going to burn out fast otherwise (already being pretty tired from my last paid job). So the first thing I did is I created a  [spreadsheet with 7 columns](https://docs.google.com/spreadsheets/d/1M_Sf0dB3gFz3YQ8I4VnbxlP8uMNFEgHb21z2Oy6QDiM/edit?usp=sharing)  for every day of a week and tried to imagine how my ideal schedule would look like. Not a fan of time-blocking but still a good exercise. 

Can't say I follow my own schedule fully or even if I think I'm going to. But I'm sure just taking time to think about your day makes you more organized.

### a plan

One of my 'meta-goals' is to choose and set up my own tech stack and practices that I will replicate quickly from project to project without wasting time. I have some version of that already, usually going with webpack + typescript + prettier + express/react + mobx. And I have a bunch of scripts that I mostly copy to a new repo when I need to start one.

This one is an example from a monorepo I have built, and it looks very similar to every repo I start:

```
{
  "start:web": "webpack serve --progress --config ./web_app/webpack.config.js ",
  "start:web:in-prod-mode": "NODE_ENV=production APP_ENV=dev webpack serve --mode production --compress --progress --config ./web_app/webpack.config.js ",
  "start:admin": "webpack serve --progress --config ./admin_app/webpack.config.js ",
  "start:android": "react-native run-android",
  "start:ios": "cd ios && pod install && cd .. && react-native run-ios --scheme appmobile-model",
  "build:web:analyze": "NODE_ENV=production webpack --config ./web_app/webpack.config.js --progress --profile --json > stats.json && npx webpack-visualizer-cli stats.json && open statistic.html",
  "build:admin": "NODE_ENV=production webpack --config ./admin_app/webpack.config.js --progress",
  "compile:proto": "./scripts/proto/compile-proto.sh",
  "compile:csp": "./scripts/gen-csp.js > ./scripts/csp.conf",
  "validate": "yarn run verify && yarn run test",
  "verify": "run-p -ln verify:*",
  "verify:prettier": "prettier -c .",
  "verify:stylelint": "stylelint '**/*.(tsx|css)'",
  "verify:ts": "tsc --noEmit",
  "verify:mobx": "node ./scripts/test_mobx_usage.js",
  "fix": "run-p -ln fix:*",
  "fix:prettier": "yarn run verify:prettier --write",
  "test": "NODE_ENV=production jest",
  "test:e2e:web": "wdio",
  "test:e2e:web-ios": "TEST_PLATFORM=web.ios wdio",
  "deps": "yarn upgrade-interactive --latest",
  "postinstall": "jetify ; patch-package ; yarn compile:proto"
}
```

But I want the whole thing to be less of a copy-paste based and I want to explore some modern tools to abstract away a lot of the manual work I'm used to, tools like 
 
- [Nx](https://nx.dev) to manage monorepos
- [NestJS](https://nestjs.com) to stop writing all the Express boilerplate every time
- [TailwindCSS](https://tailwindcss.com) because it looks like an ideal balance between flexibility and simplicity to me

This week, it will be the tech stack and breaking down tasks for Metapod (game dev meta server project).

### an emotion

It's still a bit hard to look at the bank account that's not gonna grow every month from employment income. Also, realizing that trading now is not just a side project but a means to make a reliable income.

It was tough to pass on great job opportunities. I found myself writing a cover letter for some startup looking for a founding CTO a few days ago. I managed to stop halfway through.

