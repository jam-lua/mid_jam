
Mid\_Jam
========

*NOTE:* This is still not ready. Many, if not most,
  would consider it a toy. Purely for esoteric reasons.


Usage
=====

Mid\_Jam generates functions that you could use
in a (Rack\_Jam)[https://github.com/jam-lua/rack\_jam].

```lua
  local Mid_Jam = require("mid_jam")
  local mj      = Mid_Jam.new()

  Rack_Jam.new().BEFORE(
    mj:GET("/my/:name/:obj")
      :param("name", "length at least", 1)
      :param("name", "length at most", 20)
      :param("obj",  "within", {'pet', 'candy', 'snowball'})
      :run(function (req, resp, env)
        -- do something magical
      end)
  )
```
Available HTTP\_Methods
=======================

  * HEAD
  * GET
  * POST
  * PUT
  * DELETE

Creation Your Own HTTP Method Handler
==============================

```lua
  local Mid_Jam = require("mid_jam")
  local mj      = Mid_Jam.new()

  mj:New_Method('PATCH')
  mj:PATCH("/puppy", function (req, resp, env)
    -- do something to your puppy
  end)
```

Installation
============


Haha.... good luck with that!


More to come...
============

Later.
