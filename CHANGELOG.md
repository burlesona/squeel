## 1.1.0 (unreleased)

* Deprecated core extensions. In Squeel 2.0, the DSL will be the way to
  construct queries, and Symbol/Hash extensions will go away.

## 1.0.17 (2013-02-28)

* Revert MySQL hacks, since AR did too.

## 1.0.16 (2013-02-12)

* Port workaround for MySQL's "helpful" casting behavior from Rails 3.2.12

## 1.0.15 (2013-01-23)

* Fix issue #214, don't alter table name when mergine a relation with a default
  scope

## 1.0.14 (2012-12-04 OpenHack Louisville Edition!)

* Use bind values in where_values_hash, to prep for compatibility with 3.2.10
* Allow Symbol#to_proc blocks to fall through to Array's select method

## 1.0.13 (2012-10-11)

* Allow strings in from_value. Fixes incompatibility with acts-as-taggable-on.

## 1.0.12 (2012-10-07)

* Properly uniq order_values before visiting, to fix #163
* Remove an unnecessary passthrough on String in visitor.rb. Fixes #162

## 1.0.11 (2012-09-03)

* Fixed issue #157, resolving problems when joining the same table twice.
* Allow predicates in order/select values
* Support Relation#from in Squeel DSL

## 1.0.10 (2012-09-01)

* Yanked from RubyGems.org due to semantic versioning oversight

## 1.0.9 (2012-08-06)

* Fix issue with duplication of order conditions in default_scope on AR 3.0.x

## 1.0.8 (2012-07-28)

* Fix an issue with properly casting values to column type when used
  on Rails 3.0.x.

## 1.0.7 (2012-07-14)

* Prevent reorder(nil) on reversed SQL from adding an order by id.

## 1.0.6 (2012-06-16)

* Prevent cloned KeyPaths from modifying each other. Fixes #135

## 1.0.5 (2012-06-08)

* Stop visiting group_values on merge. AR hates ARel attributes in
  group_values.

## 1.0.4 (2012-06-07)

* Fix regression in merge causing issues with scopes returning nil

## 1.0.3 (2012-06-07)

* Port fix for Rails CVE-2012-2661 to Squeel.
* Reduce risk of a potential memory leak through overzealous
  calling to to_sym.
* Allow right-hand relation conditions to prevail in Relation#merge.

## 1.0.2 (2012-05-30)

* Add groupings to DSL. Allows control of matched sets of
  parentheses in the absence of not/and/etc. Accessed via
  `_()`.
* Allow As nodes in predicates. This allows casting inside
  a where/having clause with PostgreSQL: `cast(value.as type)`
* Work around issue with Relation#count when where_values
  contains InfixOperations. Fixes #122.

## 1.0.1 (2012-05-02)

* Undefine `type` method on Stubs/KeyPaths for 1.8.x compat.

## 1.0.0 (2012-04-22)

* Official 1.0.0 release.
