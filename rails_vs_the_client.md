# Rails vs The Client

- Being able to deal with components independently of each other.
vs
- Simplicity is using simple structures.

## Speed
- Basecamp approach loses advantage over slow connection, as every click requires
talking to the server
- Ember can update the client first and notify the server later

## Optimized for
- Server style is optimized to not disrupt Rails
- Client style is optimized to simplify server logic

## Questions to ask
- Is the representation of data stable? Same display for all users? -> Server style
- Is interaction with server mostly for notification? Not asking for permission -> Client style
- Do client components interact? Automatic page updates as time passes/events
happen  -> Client style
- What do you already have? What is your in house knowledge like? Is it worth
adding a new technology to the skillset requirement? Time constraints?
- Will a hybrid approch work?

## Takeaways
- No need to redownload assets (single page or turbolinks)
- JS Frameworks still need polishing
-

www.tablexi.com/blog/category/xi-to-eye

