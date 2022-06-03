# Log of architecture decisions made

## Use CMS to store and render offers
CMS offers existing tools for rich text editing that can be used by Nonprofit representatives with only minimal training

## Use WordPress as the preferred CMS
WordPress is already an established CMS, with multiple plugin support. Access for a nonprofit user can be easily limited and granted based on external access providers. Can be self-hosted, but managed WordPress solution is generally efficient and provides added CDN and maintenance benefits

## Multiple users should be able to represent a single nonprofit organisation
We want to support bigger non-profit organisations that may have multiple employees working with the Spotlight platform, without encouraging platform and account sharing. User identity (login and personal information) should be separate from non-profit. Assigning users to non-profit organisations should be done by admins or email invites only.

## Interface should be a web application with separate pages and a shared component library
The easiest way to accommodate multiple UI pages for multiple services will be if every page is separated, but built on a shared style guide. The style guide (shared CSS styles) will ensure a consistent experience between pages. Component library in any framework would allow reusing of shared components, but should not be mandatory for each page

## Use React to build a component library and web application pages
React is an already established and well-known framework and a good default for building websites. Has support for reactive UI for web apps to be usable on mobile browsers. Each domain or feature would still be a separate web application and has the flexibility to be written in different technology if required. It would still have the same styling when reusing the style guides, without needing to directly use React components from the library

## Nonprofit Community Hub and Candidate Career Management will be delivered as one platform
Although those two use cases are separate and do not have much overlap (besides offerings service matching), there is still benefit in delivering them on one platform

## Website and application code should be hosted on cloud provisioning service
All of AWS, Google Cloud and Azure offer solutions that can host all components of the Spotlight platform, and many products are managed and do not require ongoing maintenance.

## Relational DB should be the default storage for application data
Relational DBs are proven technology, and sensible default if there are no other requirements (eg high performance processing). Managed relational databases provide adequate performance in general use cases. If Offerings are stored and rendered from CMS, most other data are well structured.

## Use Elastic (or Elastic Search) as the data store for offers matching
Elastic offers good performance when providing data recommendations and searching based on multiple criteria