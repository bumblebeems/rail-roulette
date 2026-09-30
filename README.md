# Rail Roulette

Program that selects random stations and tracks visited/unvisited status across the Victorian train network (V/Line and Metro)

## Roadmap:

1. Write backend and simple CLI interface in Go -- this will be my first time using Go, but I am interested in it for it's simple syntax (and lack of things like classes and other complicated OOP things, I struggled with those when trying to learn previously) and the fact it compiles to a single binary with no need for any external runtimes (Node, Python Interpreter, etc.)
2. Separate logic into a separate file to ease creation of future frontends -- early on I will likely have everything in one file, but I want to keep this in mind before things get too complicated and hard to pull apart
3. TUI interface in Go (Bubble Tea?)
4. Web app with frontend in Javascript/Typescript and using the pre-existing Go backend for all the logic and thinking -- this is the end goal of this project, as I foresee most people wanting to use this on their phones. Would also be an opportunity for me to learn a second language and webdev!

## WebUI

At this stage I already have a few things in mind for how I'd implement the WebUI, with the main one being that the server itself should be stateless. Visiting the site would serve a copy of the web app for your browser to cache, and everything would be done client side. This has a few benefits:

  1. There would be no need for me to add an accounts system and have to deal with all the security and privacy compliance issues that come along with that
  2. There would be minimal load on the server hosting the project
  3. From what I know this SHOULD Make it possible for the web app to work offline

There are a few things I'd need to work around with the above approach, mainly how would saves be handled without an account system? I'd store it locally on the user's browser and a feature to export all saved data a .json file will be in settings. I also have an idea for "password" system similar to how old NES/SNES games without SRAM/FRAM handled progression. This might get a bit unwieldy depending on how much data a save can hold though, so we will see about this specific point
