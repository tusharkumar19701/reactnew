## 1 What is Emmet?
Ans: Emmet is a plug in for many popular text editors which greatly improves HTML & CSS workflow.
Emmet is a free add-on for your text editor that allows you to type shortcuts that are then expanded into full pieces of code.  





## 2 Difference between library and framework
Ans: Both libraries and frameworks are reusable code written by someone else. Their purpose is to help you solve common problems in easier ways.
A library is like going to Ikea. You already have a home, but you need a bit of help with furniture. You don’t feel like making your own table from scratch. Ikea allows you to pick and choose different things to go in your home. You are in control.
A framework, on the other hand, is like building a model home. You have a set of blueprints and a few limited choices when it comes to architecture and design. Ultimately, the contractor and blueprint are in control. And they will let you know when and where you can provide your input.

Frameworks and libraries are both code written by someone else that helps you perform some common tasks in a less verbose way.
A framework inverts the control of the program. It tells the developer what they need. A library doesn’t. The programmer calls the library where and when they need it.
The degree of freedom a library or framework gives the developer will dictate how “opinionated” it is.






## 3 What are CDNs? Why are they used?
Ans: CDN stands for Content Delivery Network. It is a distributed network of servers strategically located around the world to deliver web content, such as text, images, videos, and other resources, to users based on their geographic location. The primary purpose of a CDN is to improve the performance, reliability, and efficiency of content delivery on the internet.
Here's why CDNs are used:

Faster Content Delivery: CDNs cache static content on multiple servers across different locations. When a user requests a particular piece of content, it is delivered from the nearest CDN server instead of the origin server, reducing the physical distance and consequently decreasing latency. This results in faster load times for web pages and a better user experience.

Load Balancing: CDNs distribute the load of delivering content across multiple servers. This load balancing helps prevent any single server from becoming overwhelmed with too many requests, ensuring that websites and applications remain responsive even during periods of high traffic.

Scalability: CDNs provide a scalable infrastructure, allowing websites to handle increased traffic without a significant impact on performance. This is particularly important for websites and applications that experience fluctuations in user activity or sudden traffic spikes.

Reduction in Bandwidth Costs: By offloading a significant portion of content delivery to CDN servers, the demand on the origin server's bandwidth is reduced. This can lead to cost savings for website owners, as they may be charged based on the amount of data transferred from their origin server.

Enhanced Security: CDNs can offer security features such as DDoS (Distributed Denial of Service) protection, web application firewalls, and SSL/TLS encryption. By providing an additional layer of security, CDNs help protect websites and applications from various online threats.

Global Reach: With servers located around the world, CDNs enable content to be delivered quickly to users regardless of their geographical location. This is particularly beneficial for international websites or applications with a diverse user base.

Improved Reliability and Redundancy: CDNs enhance the reliability of content delivery by providing redundancy. If one server in the CDN network fails, another server can seamlessly take over, ensuring continuous availability of content.






## 4 Why is React known as React?
Ans: React, the JavaScript library for building user interfaces, is called "React" because of its core concept: reactive programming. The name reflects the way React handles changes in a web application's state and efficiently updates the user interface to reflect those changes.

The key idea behind React is the concept of a "reactive" user interface, where the UI reacts to changes in data and updates itself automatically. When the underlying data changes, React efficiently updates only the parts of the UI that need to be changed, rather than re-rendering the entire page. This reactive approach helps in creating interactive and dynamic user interfaces with a smooth user experience.




## 5 What is crossorigin in script tag?
Ans: The crossorigin attribute in a script tag is used to control how the browser handles loading of cross-origin (external) scripts. This attribute is typically used when loading scripts from a different domain (cross-origin) to ensure proper security measures are followed.

The crossorigin attribute can take one of three values:

> anonymous: This is the default value. When set to "anonymous," the browser fetches the script without sending any credentials (like cookies or HTTP authentication) along with the request. This is suitable when you are loading a script from a different domain, and you don't need to include any credentials.
> use-credentials: When set to "use-credentials," the browser includes credentials (like cookies or HTTP authentication) with the request for the script. This is appropriate when the server hosting the script requires authentication.
> (not set): If the crossorigin attribute is not set, the browser behaves as if it's set to "anonymous."
It's important to use the crossorigin attribute correctly, especially when dealing with third-party scripts or content delivery networks (CDNs). This helps prevent certain security issues, such as cross-site scripting (XSS) attacks, by controlling how the browser interacts with external scripts and ensuring that they are loaded securely.






## 6 What is diference between React and ReactDOM ?
Ans: 
React:
Purpose: React is a JavaScript library for building user interfaces. Its primary focus is on providing a declarative syntax for creating components that represent different parts of a user interface. React allows developers to efficiently update and render UI components in response to changes in application state.
Key Concepts:
Components: Building blocks of a React application. Components encapsulate the logic and UI structure.
Virtual DOM: React uses a virtual representation of the DOM to optimize updates and improve performance.
Reconciliation: React efficiently updates the DOM by comparing the virtual DOM with the actual DOM and making minimal necessary changes.
JSX: A syntax extension for JavaScript that allows you to write HTML-like code within JavaScript.

ReactDOM:
Purpose: ReactDOM is a package specifically designed for interacting with the DOM (Document Object Model). It provides methods to render React components into the DOM, update them, and handle events.
Key Methods:
ReactDOM.render(): Takes a React element and renders it into the specified DOM container.
ReactDOM.hydrate(): Similar to render(), but used in scenarios where the server-rendered HTML needs to be preserved and React needs to take over.
ReactDOM.unmountComponentAtNode(): Removes a mounted React component from the DOM.
ReactDOM.createPortal(): Renders a child component into a different DOM subtree.






## 7 What is difference between react.development.js and react.production.js files via CDN?
Ans: react.development.js:
Debugging Features: This version includes extensive error messages and warnings in the console. It provides meaningful stack traces and warnings to aid developers in identifying and fixing issues during development.
Performance Tools: Development builds of React include additional performance monitoring and debugging tools that can help developers identify potential bottlenecks and performance issues in their applications.
File Size: The development version is larger in file size compared to the production version because it contains additional code for debugging and development tools.

react.production.js:
Minification and Optimization: The production version is minified and optimized for performance. It does not include the extensive debugging information present in the development version, making the file size smaller and the code more efficient for deployment.
Console Warnings and Errors: The production build includes less verbose error messages and warnings. It aims to be more concise and does not provide the same level of detailed information as the development build.
File Size: The production version is smaller in file size compared to the development version, making it more suitable for deployment in production environments.

Usage Recommendations: 
During development, it's common to use the development version (react.development.js) to take advantage of the debugging tools and error messages.
When deploying your application to a production environment, it's recommended to switch to the production version (react.production.js) for better performance and a smaller file size. This helps in optimizing the user experience and reducing load times.







## 8 What is async and defer?
Ans: 
async Attribute:
When you include the async attribute in a <script> tag, it indicates to the browser that the script is independent and can be executed asynchronously.
The script will not block the parsing of the HTML document. Instead, it will be fetched in the background while HTML parsing continues, and it will execute as soon as it is downloaded.
Multiple scripts with the async attribute can be downloaded concurrently, and they will execute in the order they finish downloading.

defer Attribute:
When you include the defer attribute in a <script> tag, it indicates that the script should be executed after the HTML document has been fully parsed.
Multiple scripts with the defer attribute will be executed in the order they appear in the document, after the HTML parsing is complete.
Unlike async, scripts with the defer attribute do not block HTML parsing.

Comparison:
Execution Order:
With async, scripts can execute as soon as they are downloaded, and they may not execute in the order in which they appear in the HTML document.
With defer, scripts are guaranteed to execute in the order they appear, after HTML parsing is complete.
Blocking Behavior:

async does not block HTML parsing; it allows parsing to continue while the script is being fetched.
defer also does not block HTML parsing but ensures that script execution is deferred until after parsing is complete.

Usage Considerations:
Use async when the script can be executed independently, and the order of execution doesn't matter.
Use defer when the script relies on the DOM being fully parsed, and the order of execution is important.
It's worth noting that both attributes are used to improve the loading performance of web pages by optimizing the way scripts are fetched and executed.