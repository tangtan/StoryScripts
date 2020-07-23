# Story Script (XML)

The story script is defined as an `XML` document that records story characters and their scenic interactions. We define two kinds of leaf nodes, namely `<Location />` and `<Character />`, which are under the root node `<Story />`. The `<Location />` node contains two necessary attributes: *Name* and *Sessions*. A *Session* refers to a scenic group that contains one or more *Characters*. A *Character* contains one necessary attributes: *Name*. The `<Span />` nodes represent the *Sessions*, which are characterized by a three-tuple: *Start (Time)*, *End (Time)*, and *Session (Id)*. The sample script （Redhat） is as follows:

```HTML
<?xml version="1.0" encoding="utf-8" ?>
<Story>
  <Locations>
    <Location Name="Red cap's Home" Sessions="1, 2" />
    <Location Name="Forest" Sessions="2"></Location>
    <Location Name="Grandmother's Home" Sessions="3"></Location>
  </Locations>
  <Characters>
    <Character Name="Red cap">
      <Span Start="1" End="5" Session="1"></Span>
      <Span Start="5" End="18" Session="2"></Span>
      <Span Start="18" End="22" Session="3"></Span>
    </Character>
    <Character Name="Mother">
      <Span Start="1" End="25" Session="1"></Span>
    </Character>
    <Character Name="Grandmother">
      <Span Start="10" End="15" Session="3"></Span>
    </Character> 
    <Character Name="Wolf">
      <Span Start="6" End="11" Session="2"></Span>
      <Span Start="11" End="25" Session="3"></Span>
    </Character>
  </Characters>
</Story>

```

## JSON

We also provide a simplified `JSON` format which is compatible with the `XML` document (see [iStoryline.js](https://github.com/tangtan/iStoryline.js/wiki/Story-Script)).
