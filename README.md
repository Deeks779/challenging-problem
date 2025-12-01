<h2>Most Challenging Problem Solved</h2>

<p>
  The most challenging problem I solved recently was designing a dynamic filtering feature 
  for a <strong>File Vault</strong> system while staying within a strict 
  <strong>rate limit of two requests per second</strong>.
</p>

<p>
  The filtering module needed to support multiple fields—such as 
  <em>file name, size, date, and author</em>—but sending each filter as a separate API request 
  would immediately exceed the rate limit, resulting in inconsistent or incomplete results.
</p>

<p>
  To address this, I redesigned the filtering system so that all user-selected filters were 
  combined into a single dynamic query. I implemented logic that constructs a conditional 
  <strong>SQL</strong> query object, attaching only the filters provided by the user.
</p>

<p>
  This approach allowed the frontend to send just <strong>one request</strong> while still 
  supporting complex multi-criteria searches, ensuring the solution met the rate-limit 
  constraints and significantly improved overall performance and user experience.
</p>
