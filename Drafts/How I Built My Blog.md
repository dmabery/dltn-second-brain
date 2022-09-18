I had two priorities when building this blog:

1. I wanted to learn the nitty gritty of a functioning web application.
	- How does data get sent from one place to another?
	- Where do I add all of the social share and open graph settings?
	- Etc.
2. I wanted it to be fully customizable and relatively easy to add new functionality as I come across cool things online.

Essentially, I used this project to apply the theories and skills I've been learning to create something greater than the sum of its parts and as a testing ground for anything I learn. So far, it has exceeded both of these expectations and I'm quite proud of it.

## The Stack
This blog is a Next.js application.

All blog posts and book notes are fetched from Contentful CMS. Next.js has a nifty getStaticProps function that allows you to fetch data before the page is built, making it blazing fast. 

For styling, I rely on Tailwind CSS (with some custom CSS for things like the scrollbar). Getting practice with writing vanilla CSS is important, but with the incredible libraries out there, it's much quicker and easier to change using Tailwind. If Tailwind didn't exists and Bootstrap was the only option, I probably *would've* just used vanilla CSS because as a designer, Bootstrap is not as aethetic as Tailwind. Another great thing about Tailwind is that most of the classes are named similarly (to write `display: flex`, you write `flex`), so in a way, I'm still practicing CSS.

The most important part of my blog is how I render the body content of the blog posts. I use `markdown-to-jsx` which allows me to write posts in, you guessed it, markdown, and then render those posts as JSX elements. This allows to me add custom React components wherever I want inside a blog post. Here's how it works.

## The berries to my pie
