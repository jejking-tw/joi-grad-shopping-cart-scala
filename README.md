# Welcome to Shopping Cart


*Read this in other languages: [English](README.md), [Português do Brasil](README.pt-br.md).*

This is where you can start to get familiar with the problem and what you need to run it.
This codebase is used during pairing session for JOI initiative.
It's focused on identifying code smells, refactoring and testing legacy codebase while promoting
conversations.

## Problem Statement

We have an existing shopping cart application, with a small set of eCommerce/shopping cart rules. Rules include calculation of total price, discount and loyalty points calculation. Most of the business logic is implemented in single method `ShoppingCart.checkout()`.

## Technology used

- Scala 3
- [SBT](https://www.scala-sbt.org/)

## Before the interview

Get familiar with the codebase! Make sure you have the necessary dependencies installed, and that you are able to run the tests.

## What you need to run it

- sbt available on the console
- checked out code

## Build

```console
$ sbt compile
```

## Run Tests

```console
$ sbt test
```

## Run the Sample Application

To understand how this library would be used you can check the `main` method in the `SampleApp` class. If you want to see the results, run:

```console
$ sbt run
```

## Existing Business Rules

Application code currently has the following rules:

- Calculates total price and total loyalty points earned by the customer.
- Products with product code starting with DIS_10 have a 10% discount applied.
- Products with product code starting with DIS_15 have a 15% discount applied.
- Loyalty points are earned more when the product is not under any offer.
  - Customer earns 1 point on every \$5 purchase.
  - Customer earns 1 point on every \$10 spent on a product with 10% discount.
  - Customer earns 1 point on every \$15 spent on a product with 15% discount.
