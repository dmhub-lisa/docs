---
title: regex
short_desc: regex type documentation
tags: api
path: lua_api/regex
uuid: 2282d542-28b3-1b58-9923-634991312932
public: true
private: false
---




### Functions

function **regex.MatchGroups**(str, pattern, options)
  parameter **str** *any*
  parameter **pattern** *any*
  parameter **options** *any*
  return *any*

function **regex.Match**(str, pattern)
  parameter **str** *any*
  parameter **pattern** *any*
  return *any[]*

function **regex.MatchAll**(str, pattern)
  parameter **str** *any*
  parameter **pattern** *any*
  return *any*

function **regex.ReplaceOne**(input, pattern, replacement)
  parameter **input** *string*
  parameter **pattern** *string*
  parameter **replacement** *string*
  return *string*

function **regex.ReplaceAll**(input, pattern, replacement)
  parameter **input** *string*
  parameter **pattern** *string*
  parameter **replacement** *string*
  return *string*

function **regex.Split**(input, pattern)
  parameter **input** *string*
  parameter **pattern** *string*
  return *any*
