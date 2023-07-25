# HANDBOX

## <u>1. Introduction</u>

Turbo bundles several techniques for creating fast, modern, progressively enhanced web applications without using much JavaScript. It offers a simpler alternative to the prevailing client-side frameworks which put all the logic in the front-end and confine the server side of your app to being little more than a JSON  API.

With Turbo, you let the server deliver HTML directly, which means all the logic for checking permissions, interacting directly with your domain model, and everything else that goes into programming an application can happen more or less exclusively within your favorite programming language. You're no longer mirroring logic on both sides of a JSON divide. All the logic lives on the server, and the browser deals just with the final HTML.

You can read more about the benefits of this HTML-over-the-wire approach on the [Hotwire site](https://hotwired.dev/). What follows are the techniques that Turbo brings to make this possible.

### i. Turbo Drive: Navigate within a persistent process

A key attraction with traditional single-page applications, when compared with the old-school, separate-pages approach, is the speed of navigation. SPAs get a lot of that speed from not constantly tearing down the application process, only to reinitialize it on the very next page.

Turbo Drive gives you that same speed by using the same persistent-process model, but without requiring you to craft your entire application around the paradigm. There's no client-side router to maintain, there's no state to carefully manage. The persistent process is managed by Turbo, and you write your server-side code as though you were living back in the early aughts - blissfully isolated from the complexities of today's SPA monstrosities!

This happens by intercepting all clicks on `<a href>` links to the same domain. When you click an eligible link, TurboDrive prevents the browser from following it, changes the browser's URL using the [History API](https://developer.mozilla.org/en-US/docs/Web/API/History), requests the new page using [fetch](https://developer.mozilla.org/en-US/docs/Web/API/fetch) and then renders the HTML response.

Same deal with forms. Their submissions are turned into `fetch` requests from which Turbo Drive will follow the redirect and render the HTML response.

During rendering, Turbo Drive replaces the current `<body>` element outright and merges the contents of the `<head>` element. The JavaScript window and document objects, and the `<html>` element, persist from one rendering to the next.

While it's possible to interact directly with Turbo Drive to control how visits happen or hook into the lifecycle of the request, the majority of the time this is a drop-in replacement where the speed is free just by adopting a few conventions

## <u>2. Navigate with Turbo Drive</u>

## <u>3. Decompose with Turbo Frames</u>

## <u>4. Come Alive with Turbo Streams</u>

## <u>5. Go Native on iOS & Android</u>

## <u>6. Building Your Turbo Application</u>

## <u>7. Installing Turbo in Your Application</u>
