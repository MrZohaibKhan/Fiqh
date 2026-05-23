# Fiqh Tenant Contract (v0)

## Purpose

This document defines the responsibilities, expectations, and operational boundaries between the Fiqh platform and services deployed on the platform.

The goal of Fiqh is to provide a secure, observable, and standardized platform that enables developers to deploy and operate services with minimal operational friction.

---

# Platform Responsibilities

The Fiqh platform is responsible for providing:

- standardized CI/CD workflows
- Kubernetes deployment infrastructure
- GitOps-based deployment management
- centralized observability tooling
- logging and metrics collection
- ingress and networking foundations
- secret management integrations
- deployment rollback mechanisms
- platform security policies
- reusable service templates and golden paths

---

# Tenant Responsibilities

Each tenant service is responsible for:

- application business logic
- API correctness
- service ownership
- dependency maintenance
- application-level testing
- defining service-level objectives (future)
- responding to service-related incidents
- maintaining operational documentation and runbooks

---

# Required Standards

All tenant services deployed on Fiqh must:

- expose a health endpoint
- use versioned container images
- support reproducible deployments
- include resource requests and limits
- emit structured logs
- store configuration outside application code
- define service ownership metadata
- follow platform deployment standards

---

# Security Requirements

Tenant services must not:

- run privileged containers
- use latest image tags
- store secrets in source control
- bypass platform deployment workflows
- perform manual production changes outside approved processes

---

# Operational Principles

- Git is the source of truth for platform and deployment state.
- Platform changes must be reproducible and auditable.
- Standardization is preferred over excessive customization.
- Security and observability are platform defaults, not optional add-ons.
- Platform capabilities should reduce cognitive load for developers.
- Every platform capability must solve a real operational problem.

---

# Scope

This contract is expected to evolve as the platform matures and operational requirements become more sophisticated through practical engineering experience.