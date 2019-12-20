---
layout: page
title: about me
permalink: /about
comments: true
---

<div class="row justify-content-between">
<div class="col-md-8 pr-5 profile">

<section class="row">
	<div class="col-md-6">
		<img src="{{ site.baseurl }}/media/profile/about-me-1.jpg" />
	</div>
	<div class="col-md-6">
		<h5>직업:</h5>
		<span>Java, Kotlin, Spring Boot를 주로 사용하는 Backend 개발</span>
		<h5>취미:</h5>
		<span>목공예</span>
		<h5>관심사:</h5>
		<span>Microservices Architecture, Kubernetes, Apache Kafka, Reactive, React</span>
	</div>
</section>

<hr/>

<section>
	<h4>Languages</h4>
	<span>
		<span><i class="fab fa-java"></i> Java,</span>
		<span><img class="tech-icon" src="{{ site.baseurl }}/media/icon/kotlin.png" /> Kotlin,</span>
		<span><i class="fab fa-js-square"></i> Javascript</span>
	</span>
</section>

<section>
	<h4>Frameworks</h4>
	<span>
		<span><img class="tech-icon" src="{{ site.baseurl }}/media/icon/spring-boot.png" /> Spring,</span>
		<span><i class="fab fa-react"></i> React(Beginning)</span>
	</span>
</section>

<section>
	<h4>Operations</h4>
	<span>
		<span><img class="tech-icon" src="{{ site.baseurl }}/media/icon/kubernetes.png" /> Kubernetes,</span>
		<span><i class="fab fa-docker"></i> Docker,</span>
		<span><img class="tech-icon" src="{{ site.baseurl }}/media/icon/ubuntu.png" /> Ubuntu,</span>
		<span><img class="tech-icon" src="{{ site.baseurl }}/media/icon/centos.png" /> CentOS</span>
	</span>
</section>

<section>
	<h4>Solutions</h4>
	<span>
		<span><img class="tech-icon" src="{{ site.baseurl }}/media/icon/apache-kafka.png" /> Apache Kafka,</span>
		<span><img class="tech-icon" src="{{ site.baseurl }}/media/icon/apache-ignite.png" /> Apache Ignite,</span>
		<span><img class="tech-icon" src="{{ site.baseurl }}/media/icon/hazelcast.png" /> Hazelcast,</span>
		<span><img class="tech-icon" src="{{ site.baseurl }}/media/icon/elastic.png" /> ELK Stack</span>
	</span>
</section>

</div>

<div class="col-md-4">

<div class="sticky-top sticky-top-80">
<h5>Contact</h5>

<p>광고는 사양합니다.</p>

{% assign author = site.authors['David'] %}
<a target="_blank" href="{{ author.facebook }}" class="contact-link text-primary"><i class="fab fa-facebook-square"></i></a>
<a target="_blank" href="mailto:{{ author.email }}" class="contact-link text-info"><i class="fas fa-envelope-square"></i></a>

</div>
</div>
</div>
