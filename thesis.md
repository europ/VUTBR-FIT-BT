# Continuous Integration and Automated Code Review in Open Source Projects

**Specification**:
1. Study the theoretical background behind continuous integration and automated code review.
2. Conduct research on the solutions used in popular open source projects.
3. Analyze the implementation of the "code review bot" used in ManageIQ.
4. Based on this research, propose enhancements to the implementation.
5. Implement some of the enhancements after a discussion with the project's maintainers.
6. Evaluate the enhanced developer experience achieved by these enhancements

---

### Section 1

* Introduction (Redhat,ManageIQ)

### Section 2

* **what is it ... usage ... application ... (+) and (-)**
* Continuous integration
* Automated code review

### Section 3

* Open Source
* Github
* Travis
* Ruby

### Section 4

* ManageIQ bot
* Conclusion (Redhat,ManageIQ)

---

### bibliography:

* http://www.fit.vutbr.cz/study/DP/BP.php?id=18948&file=t
* The Pragmatic Programmer, Andrew Hunt, David Thomas (ISBN-13 978-0-201-61622-4)
* Continuous Integration: Improving Software Quality and Reducing Risk, Paul M. Duvall (ISBN-13: 978-0321336385)


* https://martinfowler.com/articles/continuousIntegration.html
* https://www.thoughtworks.com/continuous-integration
* https://github.com/marketplace
* https://github.com/ManageIQ/miq_bot

---

### implementation:

* Pluggable linters - e.g. https://github.com/prontolabs/pronto
* Use of Github webhooks instead of polling - https://developer.github.com/webhooks
* Request for review - like assign
* Gitter integration - e.g. yell if master is broken
* Track dependent PRs - e.g. comment if merged
* Integrate with Github status API - https://developer.github.com/v3/repos/statuses

---

### other:
* http://guides.rubyonrails.org/
* https://apidock.com/ruby
* https://github.com/mperham/sidekiq/wiki