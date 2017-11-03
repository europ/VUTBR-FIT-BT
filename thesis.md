# Continuous Integration and Automated Code Review in Open Source Projects

**Specification**:
1. Study the theoretical background behind continuous integration and automated code review.
2. Conduct research on the solutions used in popular open source projects.
3. Analyze the implementation of the "code review bot" used in ManageIQ.
4. Based on this research, propose enhancements to the implementation.
5. Implement some of the enhancements after a discussion with the project's maintainers.
6. Evaluate the enhanced developer experience achieved by these enhancements


---

# TODO:

* bibliography VS. footnote e.g. "Travis CI" -> "https://travis-ci.org/"

---


### Section 1

* Introduction :white_check_mark:

### Section 2

* Theoretical basis
	* Continuous integration
		* what is it
		* where is it used
		* how does it work
	* Automated code review
		* what is it
		* where is it used
		* how does it work

### Section 3
* CI in Open Source projects
	* Open Source
	* Github
	* Travis
	* Jenkins
* Ruby

### Section 4

* ManageIQ bot
* Conclusion (Redhat,ManageIQ, CI, Automated Code Review)

---

### bibliography:

* The Pragmatic Programmer, Andrew Hunt, David Thomas (ISBN-13 978-0-201-61622-4)
* Continuous Integration: Improving Software Quality and Reducing Risk, Paul M. Duvall (ISBN-13: 978-0321336385)
* [Continuous Integration and Its Tools](http://ieeexplore.ieee.org.ezproxy.lib.vutbr.cz/document/6802994/)


* [Static Code Analysis Tools: Effects on
Development of Open Source Software](https://www.google.cz/url?sa=t&rct=j&q=&esrc=s&source=web&cd=1&ved=0ahUKEwj1oM78-v_WAhXGWxoKHcgBDCgQFggxMAA&url=https%3A%2F%2Frepository.tudelft.nl%2Fislandora%2Fobject%2Fuuid%3Ab157de07-e5ce-4dba-8eae-154a0002a4f5%2Fdatastream%2FOBJ%2Fdownload&usg=AOvVaw1UAyLhpanCQKOkos7vkRQy)
* http://www.fit.vutbr.cz/study/DP/BP.php?id=18948&file=t


* https://martinfowler.com/articles/continuousIntegration.html
* https://www.thoughtworks.com/continuous-integration
* https://github.com/marketplace
* https://github.com/ManageIQ/miq_bot

...

* http://cope.eecs.oregonstate.edu/CISurvey/
* https://blog.travis-ci.com/2016-07-28-what-we-learned-from-analyzing-2-million-travis-builds/
* https://inventitech.com/publications/2016_beller_gousios_zaidman_travistorrent_synthesizing_travis_ci_and_github_for_full-stack_research_on_continuous_integration.pdf
* https://peerj.com/preprints/1984.pdf
* https://is.muni.cz/th/422370/fi_b/thesis.txt

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