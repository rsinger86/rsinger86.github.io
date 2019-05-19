---
layout: page
title: Projects
permalink: /projects/
---

## Django Lifecycle

I wrote this <a href="https://github.com/rsinger86/django-lifecycle" target="_blank">package</a> to address what I saw as a weakness in Django's <a href="https://docs.djangoproject.com/en/dev/topics/signals/" target="_blank">built-in approach</a> to model lifecycle events, which dispatches to a handler outside the model class. My package provides a decorator interface to declaritively describe when methods on the model should fire in response to lifecycle events, optionally predicated on field changes.

Django is a great framework, but lacking a declaritive lifecycle interface -- critical for managing complexity as projects evolve -- seemed like a weak point relative to <a href="https://guides.rubyonrails.org/active_record_callbacks.html" target="_blank">Rails</a> for sophisticated, enterprise-scale apps.

## Django REST - FlexFields

REST is a great pattern, providing UI clients with Google Maps-like navigation of your business domain and letting them focus on providing a great end-user experience. However, in service architecutures where many clients with different use cases are calling upon your REST services, it can be useful to offer them slightly different resource representations on the fly, rather than having to add a multitude of resources to the REST interface.

This <a href="https://github.com/rsinger86/drf-flex-fields" target="_blank">package</a> makes it easy to expand nested resource, omit fields or specify only the fields needed for a given use case when using <a href="https://www.django-rest-framework.org/" target="_blank">Django REST Framework</a>. This is one of the problems that <a href="https://jsonapi.org/" target="_blank">JSON:API</a> solves, but you may find it difficult to implement its spec or find its format too verbose. This project is meant to offer a simple way to provide some JSON:API/GraphQL-like functionality.



