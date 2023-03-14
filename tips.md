# A collection of tips shared from multiple bloggers

[Source:  Micah Van Deusen Blog ](https://micahvandeusen.com/burp-suite-certified-practitioner-exam-review/)

### Tip 1

Identify the new functionality. Each of the applications across the lab and exam use the same exact base blogging site. Because of this you can determine any additional functionality or differences at each new step. If you get access to a user account you should then look at what additional functionality is exposed that wasn’t accessible unauthenticated.

### Tip 2

Use selective scanning and start it as soon as possible. Automated scanning takes its time. As you’re going through the application get it started right away. In addition, focus on any inputs. PortSwigger has a guide on scanning specific inputs here: [https://portswigger.net/web-security/reference/augmenting-your-manual-testing-with-burp-scanner](https://portswigger.net/web-security/reference/augmenting-your-manual-testing-with-burp-scanner). In addition, create some scanning configurations ahead of time for select vulnerabilities you want to look for. That will speed up the scanning as well.

### Tip 3

Search the PortSwigger documentation and labs. You will likely want proof of concept code to exploit vulnerabilities. However, for a lot of this you can just as easily copy it from the solutions of related labs and modify it for your specific use case. There are few, if any, curve balls of anything not covered in the labs. Because of that they are great reference to look at during the exam.

### Tip 4

Don’t get tunnel vision. The reason I failed one of my attempts was that I got stuck thinking the new functionality had to be one type of vulnerability when it was something completely different. If you don’t make any progress, take a step back, and then see what other type of vulnerability it might be. There also may be hints in the wording of things as to what the vulnerability is or what may be happening behind the scenes.

### Tip 5

Focus on the vulnerabilities relevant to the stage you are on. Just going through the list of lab categories, not using any knowledge from what I saw on the exam itself, we can categorize them into what you should be looking for when. Don’t go looking for command injection at the very start.

| Category | Stage 1 | Stage 2 | Stage 3 |
| --- | --- | --- | --- |
| SQL Injection |     | ✔️  | ✔️  |
| Cross-site scripting | ✔️  | ✔️  |     |
| Cross-site request forgery (CSRF) | ✔️  | ✔️  |     |
| Clickjacking | ✔️  | ✔️  |     |
| DOM-based vulnerabilities | ✔️  | ✔️  |     |
| Cross-origin resource sharing (CORS) | ✔️  | ✔️  |     |
| XML external entity (XXE) injection |     |     | ✔️  |
| Server-side request forgery (SSRF) |     |     | ✔️  |
| HTTP request smuggling | ✔️  | ✔️  |     |
| OS command injection |     |     | ✔️  |
| Server-side template injection |     |     | ✔️  |
| Directory traversal |     |     | ✔️  |
| Access control vulnerabilities | ✔️  | ✔️  |     |
| Authentication | ✔️  | ✔️  |     |
| Web cache poisoning | ✔️  | ✔️  |     |
| Insecure deserialization |     |     | ✔️  |
| HTTP Host header attacks | ✔️  | ✔️  |     |
| OAuth authentication | ✔️  | ✔️  |     |
| File upload vulnerabilities |     |     | ✔️  |
| JWT | ✔️  | ✔️  |     |

### Tip 6

They tell you in the instructions that the low privilege user is possibly in this [list](https://portswigger.net/web-security/authentication/auth-lab-usernames) and the password in this [list](https://portswigger.net/web-security/authentication/auth-lab-passwords). There is probably a reason they mention it and it doesn’t take long looking for user enumeration and to perform password spraying. In general, most wording throughout the instructions and the exam pages are there for a reason and may be hints for what you should do.

### Tip 7

Take the practice exam. It’s a good way to get familiar with the exam format.

### Tip 8

Register using the same email for the proctoring site. The whole proctoring process is odd and I think it has thrown a couple people off. It is just used for photo and ID verification to enter a password to start the exam. For me, the proctoring site didn’t recognize the exam unless it was under the same exact email. This is just from personal experience though. It does make me question how the integrity of the certificate will hold up as cheating the proctoring seems trivial. However, that’s a much bigger problem that not even full exam length proctoring completely solves.

### Tip 9

Check the website occasionally after passing the exam. I think clearer instruction after the exam would be helpful. You have to wait until the end of the full 4 hours to know the next step of waiting 24-48 hours for the results and proctoring to be verified. I was expecting an email when that happened and waited several days for it. Turns out you have to login to the PortSwigger site to get the final results.


