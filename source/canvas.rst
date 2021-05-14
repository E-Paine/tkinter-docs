******
Canvas
******

.. raw:: html

    <style> .c3c3c3 {color:#c3c3c3} </style>

.. role:: c3c3c3

.. class:: Canvas(master=None, cnf={}, **kw)

    *master* is the parent widget of this canvas. If ``None``, tkinter will
    attempt to use the :term:`default root <default root>`.
    
    *cnf* and *kw* are both used to specify widget options (see below). For
    example, ``Canvas(root, {"bg": "white"})`` and
    ``Canvas(root, bg="white")`` are equivalent.
    
    Widget options:
    
    | *background=*
    | *bg=*
    | Specifies the normal background color to use when displaying the widget.
      The default value is the platform default background colour.

    | *borderwidth=*
    | *bd=*
    | Specifies a non-negative value indicating the width of the 3-D border to
      draw around the outside of the widget (if such a border is being drawn;
      the *relief* option typically determines this). The value may also be
      used when drawing 3-D effects in the interior of the widget. The value
      may be any valid :ref:`Tk length <lengths>`. The default value is 0.
    
    | *closeenough=*
    | Specifies a floating-point value indicating how close the mouse cursor
      must be to an item before it is considered to be “inside” the item.
      Defaults to 1.0.
    
    | *confine=*
    | Specifies a boolean value that indicates whether or not it should be
      allowable to set the canvas's view outside the region defined by the
      scrollRegion argument. If the value is ``True``, the view will be
      constrained within the scroll region. The default value is ``True``.
    
    | *cursor=*
    | Specifies the mouse cursor to be used for the widget. The value may be
      any valid :ref:`Tk cursor <cursors>`. If an empty string is given, the
      widget should defer to its parent for cursor specification. The default
      value is to defer.
    
    | *height=*
    | Specifies a desired height that the canvas widget should request from
      its geometry manager. The value may be in any of the forms described in
      the :ref:`coordinates <coordinates>` section below. The default value is
      "7c".
      
    | *highlightbackground=*
    | Specifies the color to use as a border highlight when the widget does
      not have focus. The default value is the platform default background
      colour.
    
    | *highlightcolor=*
    | Specifies the color to use as a border highlight when the widget has
      focus. The default values are as follows:
      
      +---------+------------------------------------+
      | MacOS   | platform default foreground colour |
      +---------+------------------------------------+
      | Unix    | black                              |
      +---------+------------------------------------+
      | Windows | platform default 'frame' colour    |
      +---------+------------------------------------+
    
    | *highlightthickness=*
    | Specifies a non-negative value indicating the width of the highlight
      rectangle to draw around the outside of the widget when it has focus.
      The value may be any valid :ref:`Tk length <lengths>`. If the value is
      zero, no focus highlight is drawn around the widget. The default values
      are as follows:
      
      +---------+---+
      | MacOS   | 3 |
      +---------+---+
      | Unix    | 1 |
      +---------+---+
      | Windows | 2 |
      +---------+---+
    
    | *insertbackground=*
    | Specifies the color to use as background in the area covered by the
      insertion cursor. This color will normally override either the normal
      background for the widget (or the selection background if the insertion
      cursor happens to fall in the selection). The default values are as
      follows:
      
      +---------+------------------------------------+
      | MacOS   | black                              |
      +---------+------------------------------------+
      | Unix    | black                              |
      +---------+------------------------------------+
      | Windows | platform default foreground colour |
      +---------+------------------------------------+
    
    | *insertborderwidth=*
    | Specifies a non-negative value indicating the width of the 3-D border to
      draw around the insertion cursor. The value may be any valid
      :ref:`Tk length <lengths>`. The default value is 0.
    
    | *insertontime=*
    | Specifies a non-negative integer value indicating the number of
      milliseconds the insertion cursor should remain “off” in each blink
      cycle. If this option is zero then the cursor does not blink: it is on
      all the time. The default value is 300.
    
    | *insertontime=*
    | Specifies a non-negative integer value indicating the number of
      milliseconds the insertion cursor should remain “on” in each blink
      cycle. The default value is 600.
    
    | *insertwidth=*
    | Specifies a value indicating the total width of the insertion cursor.
      The value may be any valid :ref:`Tk length <lengths>`. If a border has
      been specified for the insertion cursor (using the *insertborderwidth*
      option), the border will be drawn inside the width specified by the
      *insertwidth* option. The default value is 2.
    
    | *relief=*
    | Specifies the 3-D effect desired for the widget. The value may be any
      valid :ref:`Tk relief <reliefs>`. The value indicates how the interior
      of the widget should appear relative to its exterior; for example,
      raised means the interior of the widget should appear to protrude from
      the screen, relative to the exterior of the widget. The default value
      is "flat".
    
    | *scrollregion=*
    | Specifies a list with four coordinates describing the left, top, right
      and bottom coordinates of a rectangular region. This region is used for
      scrolling purposes and is considered to be the boundary of the
      information in the canvas. Each of the coordinates may be in any of the
      forms described in the :ref:`coordinates <coordinates>` section below.
      An empty string will make the scrollregion match the width and height of
      the canvas. The default value is an empty string.
    
    | *selectbackground=*
    | Specifies the background color to use when displaying selected items.
      The default values are as follows:
      
      +---------+-----------------------------------+
      | MacOS   | platform default selection colour |
      +---------+-----------------------------------+
      | Unix    | #c3c3c3 (:c3c3c3:`light grey`)    |
      +---------+-----------------------------------+
      | Windows | platform default highlight colour |
      +---------+-----------------------------------+
    
    | *selectborderwidth=*
    | Specifies a non-negative value indicating the width of the 3-D border to
      draw around selected items. The value may be any valid
      :ref:`Tk length <lengths>`. The default value is 0.
    
    | *selectforeground=*
    | Specifies the foreground color to use when displaying selected items.
      The default values are as follows:
      
      +---------+----------------------------------------+
      | MacOS   | platform default selection text colour |
      +---------+----------------------------------------+
      | Unix    | black                                  |
      +---------+----------------------------------------+
      | Windows | platform default highlight text colour |
      +---------+----------------------------------------+
    
    | *state=*
    | Modifies the default state of the canvas where state may be set to one
      of: "normal", "disabled", or "hidden". Individual canvas objects all
      have their own state option which may override the default state. Many
      options can take separate specifications such that the appearance of the
      item can be different in different situations. The options that start
      with "active" control the appearance when the mouse pointer is over it,
      while the options starting with "disabled" control the appearance when
      the state is disabled. Canvas items which are disabled will not react to
      canvas bindings. The default value is "normal".
    
    | *takefocus=*
    | Determines whether the window accepts the focus during keyboard
      traversal (e.g., Tab and Shift-Tab). Before setting the focus to a
      window, the traversal scripts consult the value of the *takefocus*
      option. A value of ``False`` means that the window should be skipped
      entirely during keyboard traversal. ``True`` means that the window
      should receive the input focus as long as it is viewable (it and all of
      its ancestors are mapped). An empty string for the option means that the
      traversal scripts make the decision about whether or not to focus on the
      window: the current algorithm is to skip the window if it is disabled,
      if it has no key bindings, or if it is not viewable.
      
    | If any other value is given, then the traversal scripts take the value,
      append the name of the window to it (with a separator space), and
      evaluate the resulting string as a Tcl script. The script must return 0,
      1, or an empty string: a 0 or 1 value specifies whether the window will
      receive the input focus, and an empty string results in the default
      decision described above. The default value is an empty string.
      
    .. note::
        This interpretation of the option is defined entirely by the Tcl
        scripts that implement traversal: the widget implementations ignore
        the option entirely, so you can change its meaning if you redefine
        the keyboard traversal scripts.
    
    | *width=*
    | Specifies a desired width that the canvas widget should request from its
      geometry manager. The value may be in any of the forms described in the
      :ref:`coordinates <coordinates>` section below. The default value is
      "10c".
    
    | *xscrollcommand=*
    | Specifies the command used to communicate with horizontal scrollbars.
      When the view in the widget's window changes (or whenever anything else
      occurs that could change the display in a scrollbar, such as a change
      in the total size of the widget's contents), the widget will call the
      function with two numbers as arguments.
      
    | Each of the numbers is a fraction between 0 and 1, which indicates a
      position in the document. 0 indicates the beginning of the document,
      1 indicates the end, .333 indicates a position one third the way through
      the document, and so on. The first number indicates the first
      information in the document that is visible in the window, and the
      second number indicates the information just after the last portion that
      is visible.
      
    | Typically, the *xscrollcommand* will be set to :mod:`Scrollbar.set`:
      this will cause the scrollbar to be updated whenever the view in the
      window changes. If this option is not specified, then no command will be
      executed. The default value is to call no function.
      
    .. note::
        Tkinter does not convert these numbers to Python floats for you, and
        instead leaves them as strings.
    
    | *xscrollincrement=*
    | Specifies an increment for horizontal scrolling, in the form of any
      valid :ref:`Tk length <lengths>`. If the value of this option is
      greater than zero, the horizontal view in the window will be constrained
      so that the canvas x coordinate at the left edge of the window is always
      an even multiple of *xscrollincrement*; furthermore, the units for
      scrolling (e.g., the change in view when the left and right arrows of a
      scrollbar are selected) will also be *xscrollincrement*. If the value of
      this option is less than or equal to zero, then horizontal scrolling is
      unconstrained. The default value is 0.
    
    | *yscrollcommand=*
    | Specifies the prefix for a command used to communicate with vertical
      scrollbars. This option is treated in the same way as the
      *xscrollcommand* option, except that it is used for vertical scrollbars
      and is provided by widgets that support vertical scrolling. See the
      description of *xscrollcommand* for details on how this option is used.
      The default value is to call no function.
    
    | *yscrollincrement=*
    | Specifies an increment for vertical scrolling, in the form of any valid
      :ref:`Tk length <lengths>`. If the value of this option is greater than
      zero, the vertical view in the window will be constrained so that the
      canvas y coordinate at the top edge of the window is always an even
      multiple of *yscrollincrement*; furthermore, the units for scrolling
      (e.g., the change in view when the top and bottom arrows of a scrollbar
      are selected) will also be *yscrollincrement*. If the value of this
      option is less than or equal to zero, then vertical scrolling is
      unconstrained. The default value is 0.
    
    .. method:: addtag_above(newtag, tagOrId)
        
        For each item just after (above) the one given by *tagOrId* in the
        display list, add *newtag* to the list of tags associated with the
        item if it is not already present on that list. It is possible that
        no items will be above the item given by *tagOrId*, in which case the
        command has no effect. If *tagOrId* denotes more than one item, then
        the last (topmost) of these items in the display list is used.

.. _coordinates:

Coordinates
-----------

TODO
