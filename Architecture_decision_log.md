# Log of architecture decisions made

## Use CMS to store and render offers
CMS offers existing tools for rich text editing that can be used by Nonprofit representatives with only minimal training

## Use Wordpress as preferred CMS
Wordpress is already established CMS, with multiple plugin support. Access for nonprofit can be easily limited, and granted based on external access providers. Can be self-hosted, but managed Wordpress solution is generally efficient and provides added CDN and maintenance benefits

## Multiple users should be able to represent single nonprofit organisation
We want to support bigger non profit organisations that may have multiple employees working with Spotlight platform, without encouraging platform and account sharing. User identity (login and personal information) should be separate from non profit. Assigning users to non profit should be done by admins or email invites only.

## Interface should be web application with separate pages and shared component library
The easiest way to accomodate multiple UI pages for multiple services will be if every page is separated, but build on shared style guide. Style guide (shared css styles) will ensure consistent experience between pages. Component library in any framework would allow reusing of shared componenets, but should not be mandatory for each page

## Use React to build component library and and web application pages
React is already established and well known framework and a good default for building websites. Has support for reactive UI for web app to be usable on mobile browsers. Each domain/feature would still be a separate web application, and if React is not good fit for it, it might be built using different technology, but has same styling (does not have to reuse components)

## Nonprofit Community Hub and Candidate Career Management will be delivered as one platform
Although those two use cases are separate and do not have much overalp (beside offerings matching), there is still benefit in delivering them on one platform

## Website and application code should be hosted on of existing cloud providers
Both AWS, Google Cloud and Azure offer solutions that are able to host all components of Spotlight platform, and many products are managed and do not require ongoing maintenance. 

## Relational DB should be default storage for application data
Relational DBs are proven technolgy, and sensible default if there are no other requirements (eg high performance processing). Managed relational databases provide adequate performance in general use cases. If Offerings are stored and rendered from CMS, most other data are actually well structured.

## Use Elastic (or Elastic Search) as data store for offers matching
Elastic offers good performance when providing data recommendations and searching based on multiple criteria


