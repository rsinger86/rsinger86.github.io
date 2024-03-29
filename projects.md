---
layout: page
title: Projects
permalink: /projects/
---

<!---
## Disqors

I made this [web app](https://www.disqors.com/) to scratch an itch from the heyday of blogging -- before Twitter became the public forum for political and social commentary. I've always found writing on the internet most interesting when authors engage with each other's arguments, so I built a backend in Python that seeks to surface and connect those articles into a discussion graph. Seeded by a predefined list of sources, it crawls and parses through articles and uses various heuristics, [PageRank](https://en.wikipedia.org/wiki/PageRank)-inspired algorithms and NLP techniques to measure the strength of connections and the quality of content. The frontend is written in TypeScript/Angular.
--->

## Django Lifecycle

I wrote this <a href="https://github.com/rsinger86/django-lifecycle" target="_blank">package</a> to address what I saw as a weakness in Django's <a href="https://docs.djangoproject.com/en/dev/topics/signals/" target="_blank">built-in approach</a> to model lifecycle events, which dispatches to a handler outside the model class. My package provides a decorator interface to declaritively describe when methods on the model should fire in response to lifecycle events, optionally predicated on field changes.

Django is a great framework, but lacking a declaritive lifecycle interface -- critical for managing complexity as projects evolve -- seemed like a weak point versus <a href="https://guides.rubyonrails.org/active_record_callbacks.html" target="_blank">Rails</a> for growing sophisticated, enterprise-scale apps.

## Django REST - Flex Fields

REST is a great pattern, providing UI clients with Google Maps-like navigation of your business domain and letting them focus on providing a great end-user experience. However, in service architecutures where many clients with different use cases are calling upon your REST services, it can be useful to offer them slightly different resource representations on the fly, rather than having to add a multitude of resources to the REST interface.

This <a href="https://github.com/rsinger86/drf-flex-fields" target="_blank">package</a> makes it easy to expand nested resource, omit fields or specify only the fields needed for a given use case when using <a href="https://www.django-rest-framework.org/" target="_blank">Django REST Framework</a>. This is one of the problems that <a href="https://jsonapi.org/" target="_blank">JSON:API</a> solves, but you may find it difficult to implement its spec or find its format too verbose. This project is meant to offer a simple way to provide some JSON:API/GraphQL-like functionality.


## Django REST - Access Policy

This <a href="https://github.com/rsinger86/drf-access-policy" target="_blank">package</a> provides declarative, explicit authorization for Django REST Framework projects. I really like how AWS designed its <a href="https://aws.amazon.com/iam/" target="_blank">Identity Access Management</a>
 (IAM) service -- powerful and flexible, combining context-based and role-based access rules in JSON policies. This package is inspired and partly modeled after IAM. Programmer error and confusion can be a major security vulnerability, and I've tried to provide a higher-level syntax that allows developers (and maybe even non-technical stakeholders) to focus on the rules of the business, not the code. Access policies are also JSON-serializable, allowing them to be stored outside the codebase and injected dynamically. You can change access rules without redeploying code, a key benefit for complex enterprise systems that are always changing.

## Django REST - Typed

The idea of using Python's type annotations during runtime for data validation has taken off in more recent projects (<a href="https://docs.apistar.com/" target="_blank">API Star</a>, <a href="https://github.com/tiangolo/fastapi" target="_blank">FastAPI</a>). As a big fan of Django's batteries-included approach, I wanted to see this feature in REST Framework. This project adds a couple of decorators to enable this feature. Mostly, this <a href="https://github.com/rsinger86/drf-typed" target="_blank">project</a> is just an adapter to Django REST's existing serializer fields, so they can be used to automatically validate view parameters. It also allows use of type annotations as shorthand for declaring serializer fields.

## DTO Classes

This <a href="https://github.com/rsinger86/dto-classes" target="_blank">project</a> is a TypeScript library for modelling data transfer objects in HTTP JSON APIs, especially <a href="https://nestjs.com/" target="_blank">NestJS</a>-powered ones. It provides static types by default, which makes it easy to integrate with NestJS's pipe validation. The developer interface is much closer to popular Python parsing libraries like DRF and Pydantic, while the Node ecosystem seems to favor <a href="https://github.com/colinhacks/zod" target="_blank">method chaining</a> and <a href="https://github.com/typestack/class-validator" target="_blank">decorators</a>.

