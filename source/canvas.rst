.. raw:: html

    <style> .c3c3c3 {color:#c3c3c3} </style>

.. role:: c3c3c3

******
Canvas
******

.. class:: Canvas(master=None, cnf={}, **kw)

    Create a canvas widget for drawing graphics.

    *master* is the parent widget of this canvas. If ``None``, tkinter will
    attempt to use the :term:`default root <default root>`.

    *cnf* and *kw* are both used to specify widget options (see below). For
    example, ``Canvas(root, {"bg": "white"})`` and
    ``Canvas(root, bg="white")`` are equivalent.

    Widget options:

    | *background=*
    | *bg=*
    | Specifies the normal background colour to use when displaying the
      widget. The given value may be any valid :ref:`Tk colour <colours>`. The
      default value is the platform default background colour.

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
    | Specifies the colour to use as a border highlight when the widget does
      not have focus. The given value may be any valid
      :ref:`Tk colour <colours>`. The default value is the platform default
      background colour.

    | *highlightcolor=*
    | Specifies the colour to use as a border highlight when the widget has
      focus. The given value may be any valid :ref:`Tk colour <colours>`. The
      default values are as follows:

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
    | Specifies the colour to use as background in the area covered by the
      insertion cursor. The given value may be any valid
      :ref:`Tk colour <colours>`. This colour will normally override either
      the normal background for the widget (or the selection background if the
      insertion cursor happens to fall in the selection). The default values
      are as follows:

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
    | Specifies the background colour to use when displaying selected items.
      The given value may be any valid :ref:`Tk colour <colours>`. The default
      values are as follows:

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
    | Specifies the foreground colour to use when displaying selected items.
      The given value may be any valid :ref:`Tk colour <colours>`. The default
      values are as follows:

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

    .. method:: addtag_all(newtag)

        For every item, add *newtag* to the list of tags associated with the
        item if it is not already present on that list. It is possible that
        there are no items, in which case the command has no effect.

    .. method:: addtag_below(newtag, tagOrId)

        For each item just before (below) the one given by *tagOrId* in the
        display list, add *newtag* to the list of tags associated with the
        item if it is not already present on that list. It is possible that
        no items will be below the item given by *tagOrId*, in which case the
        command has no effect. If *tagOrId* denotes more than one item, then
        the first (lowest) of these items in the display list is used.

    .. method:: addtag_closest(newtag, x, y, halo=None, start=None)

        For the item closest to the point given by x and y, add *newtag* to
        the list of tags associated with the item if it is not already present
        on that list. It is possible that there are no items, in which case
        the command has no effect. If more than one item is at the same
        closest distance (e.g. two items overlap the point), then the top-most
        of these items (the last one in the display list) will have the new
        tag applied.

        If *halo* is specified, then it must be a non-negative
        :ref:`length <lengths>`. Any item closer than *halo* to the point is
        considered to overlap it. All items overlapping the halo are treated
        as if they have a distance of 0 from the given point.

        If *start* is specified, it names an item using a tag or id (if by
        tag, it selects the bottom / first item in the display list with the
        given tag). Instead of adding *newtag* to the topmost closest item,
        this will tag the topmost closest item that is below *start* in the
        display list; if no such item exists, then it will behave as if the
        *start* argument had not been specified.

    .. method:: addtag_enclosed(newtag, x1, y1, x2, y2)

        For each item completely enclosed within the rectangular region given
        by *x1*, *y1*, *x2*, and *y2*, add *newtag* to the list of tags
        associated with the item if it is not already present on that list. It
        is possible that no items lie fully in this region, in which case the
        command has no effect. ``(x1, y1)`` must be the top-left corner of the
        region and ``(x2, y2)`` the bottom-right.

    .. method:: addtag_overlapping(newtag, x1, y1, x2, y2)

        For each item overlapping the rectangular region given by *x1*, *y1*,
        *x2*, and *y2*, add *newtag* to the list of tags associated with the
        item if it is not already present on that list. It is possible that no
        items overlap this region, in which case the command has no effect.
        ``(x1, y1)`` must be the top-left corner of the region and
        ``(x2, y2)`` the bottom-right.

    .. method:: addtag_withtag(newtag, tagOrId)

        For each item specified by *tagOrId*, add *newtag* to the list of tags
        associated with the item if it is not already present on that list. It
        is possible that no items have this tag / id, in which case the
        command has no effect.

    .. method:: bbox(*args)

        Returns a tuple with four integers giving an approximate bounding box
        for all the items given in *args*. The tuple has the form
        ``(x1, y1, x2, y2)``, such that the drawn areas of all the given
        elements are within the region bounded by x1 on the left, x2 on the
        right, y1 on the top, and y2 on the bottom. The return value may
        overestimate the actual bounding box by a few pixels. If no items
        match any of the tagOrId arguments or if the matching items have empty
        bounding boxes (i.e. they have nothing to display) then ``None`` is
        returned.

    .. method:: canvasx(self, screenx, gridspacing=None)

        Given a window x-coordinate in the canvas *screenx*, this command
        returns the canvas x-coordinate that is displayed at that location. If
        *gridspacing* is specified, then the canvas coordinate is rounded to
        the nearest multiple of *gridspacing* units.

    .. method:: canvasy(screeny, gridspacing=None)

        Given a window y-coordinate in the canvas *screeny*, this command
        returns the canvas y-coordinate that is displayed at that location. If
        *gridspacing* is specified, then the canvas coordinate is rounded to
        the nearest multiple of *gridspacing* units.

    .. method:: coords(*args)

        Query or modify the coordinates that define an item. The first
        argument should always be the tag / id of a canvas item. If no
        coordinates are specified (i.e. the only argument given is the item
        tag / id), this command returns a tuple whose elements are the
        coordinates of the item.

        If coordinates are specified, then they replace the current
        coordinates for the given item. If the tag / id refers to multiple
        items, then the bottom / first one in the display list is used.

        .. note::

            For rectangles, ovals and arcs the returned list of coordinates
            has a fixed order, namely the left, top, right and bottom
            coordinates, which may not be the order originally given. Also
            the coordinates are always returned in screen units with no units
            (that is, in pixels). So if the original coordinates were
            specified for instance in centimeters or inches, the returned
            values will nevertheless be in pixels.

    .. method:: create_arc(*args, **kw)

        Draw an arc, chord or pieslice. Returns the item id.

        | *dash=*
        | *activedash=*
        | *disableddash=*
        | These options specifies dash patterns for the normal, active and
          disabled states of the arc (correspondingly). The value may be any
          valid :ref:`Tk dash style <dashes>`. The default value is a solid
          outline.

        | *dashoffset=*
        | The starting offset in pixels into the pattern provided by the
          *dash* option. *dashoffset* is ignored if there is no *dash*
          pattern. The offset may have any of the forms described in the
          :ref:`coordinates <coordinates>` section below. The default value is
          0.

        | *extent=*
        | Specifies the size of the angular range occupied by the arc. The
          arc's range extends for the given number of degrees
          counter-clockwise from the starting angle given by the *start*
          option. The value may be negative. If it is greater than 360 or less
          than -360, then degrees modulo 360 is used as the extent. The
          default value is 90.

        | *fill=*
        | *activefill=*
        | *disabledfill=*
        | Specifies the colour to be used to fill arc's area in its normal,
          active and disabled states (correspondingly). The given value may be
          any valid :ref:`Tk colour <colours>`. If the value is an empty
          string, then the arc will not be filled (i.e. it will be
          transparent). The default value is an empty string.

        | *offset=*
        | Specifies the offset of stipples. The offset value can be of the
          form ``"x,y"`` or side, where side can be **n**, **ne**, **e**,
          **se**, **s**, **sw**, **w**, **nw**, or **center**. In the first
          case, the origin is the origin of the canvas itself, but putting #
          in front of the coordinate pair indicates using the current window's
          origin instead. For canvas objects, the *offset* option is used for
          stippling as well. The default value is ``"0,0"``.

        .. warning::
            Stipple offsets are only supported on Unix; they are silently
            ignored on other platforms.

        .. note::
            A Python tuple of ``(x, y)`` cannot be given and instead must be
            manually formatted to string of the correct format (``"x,y"`` or
            ``"#x,y"``).

        | *outline=*
        | *activeoutline=*
        | *disabledoutline=*
        | These options specifies the color that should be used to draw the
          outline of the arc in its normal, active and disabled states
          (correspondingly). The given value may be any valid
          :ref:`Tk colour <colours>`. If color is specified as an empty string
          then no outline is drawn for the arc. The default values are as
          follows:

          +---------+------------------------------------+
          | MacOS   | platform default foreground colour |
          +---------+------------------------------------+
          | Unix    | black                              |
          +---------+------------------------------------+
          | Windows | platform default foreground colour |
          +---------+------------------------------------+

        | *outlineoffset=*
        | Specifies the offset of the stipple pattern used for outlines, in
          the same way that the *offset* option controls fill stipples. See
          the *offset* option for a description of the syntax of offset. The
          default value is ``"0,0"``.

        | *outlinestipple=*
        | *activeoutlinestipple=*
        | *disabledoutlinestipple=*
        | This option specifies stipple patterns that should be used to draw
          the outline of the arc in its normal, active and disabled states
          (correspondingly). It indicates that the outline for the arc should
          be drawn with a stipple pattern and specifies the stipple pattern to
          use. The given value may be any valid
          :ref:`Tk Bitmap <bitmaps>`. If the *outline* option has not been
          specified then this option has no effect. If the value is an empty
          string, then the outline is drawn in a solid fashion. The default
          value is an empty string.

        .. warning::
            Stipples are not well supported on platforms other than Unix.

        | *stipple=*
        | *activestipple=*
        | *disabledstipple=*
        | This option specifies stipple patterns that should be used to fill
          the item in its normal, active and disabled states
          (correspondingly). The given value may be any valid
          :ref:`Tk Bitmap <bitmaps>`. If the *fill* option has not been
          specified then this option has no effect. If the value is an empty
          string, then filling is done in a solid fashion. The default value
          is an empty string.

        .. warning::
            Stipples are not well supported on platforms other than Unix.

        | *start=*
        | Specifies the beginning of the angular range occupied by the arc.
          The value is given in degrees measured counter-clockwise from the
          3-o'clock position; it may be either positive or negative. The
          default value is 0.

        | *state=*
        | This allows the arc to override the canvas widget's global *state*
          option. It takes the same values: normal, disabled or hidden. An
          empty string will defer to the canvas widget's state. The default
          value is an empty string.

        | *style=*
        | Specifies how to draw the arc. If type is **pieslice** then the
          arc's region is defined by a section of the oval's perimeter plus
          two lines between the center of the oval and each end of the
          perimeter section. If type is **chord** then the arc's region is
          defined by a section of the oval's perimeter plus a single line
          connecting the two end points of the perimeter section. If type is
          **arc** then the arc's region consists of a section of the perimeter
          alone. In this last case the *fill* option is ignored. The default
          value is **pieslice**.

        | *tags=*
        | Specifies one or more tags to apply to the arc. When used in
          :mod:`Canvas.itemconfigure`, this replaces any existing tags for the
          arc. An empty list may also be specified. The default value is an
          empty list.

        | *width=*
        | *activewidth=*
        | *disabledwidth=*
        | Specifies the width of the outline to be drawn around the arc's
          region, in its normal, active and disabled states
          (correspondingly). The value may be in any of the forms described in
          the :ref:`coordinates <coordinates>` section below. If the *outline*
          option has been specified as an empty string, then this option has
          no effect. The default value is 1.

        .. note::
            Wide outlines will be drawn centered on the edges of the arc's
            region.

    .. method:: create_bitmap(*args, **kw)

        | *anchor=*
        | The given value determines how to position the item relative to the
          positioning coordinate for the bitmap; it may have any valid
          :ref:`Tk anchor <anchors>`. For example, if the value is **center**
          then the item is centered on the point; if the value is **n** then
          the item will be drawn so that its top center point is at the
          positioning coordinate. The default value is **center**.

        | *background=*
        | *activebackground=*
        | *disabledbackground=*
        | Specifies the color to use for each of the bitmap's “0” valued
          pixels in its normal, active and disabled states (correspondingly).
          The given value may be any valid :ref:`Tk colour <colours>`. If the
          value is an empty string, then nothing is displayed where the bitmap
          pixels are 0; this produces a transparent effect. The default value
          is an empty string.

        | *bitmap=*
        | *activebitmap=*
        | *disabledbitmap=*
        | Specifies the bitmap to display in its normal, active and disabled
          states (correspondingly). The given value may be any valid
          :ref:`Tk Bitmap <bitmaps>`. An empty string specifies no bitmap. The
          default value is an empty string.

        | *foreground=*
        | *activeforeground=*
        | *disabledforeground=*
        | Specifies the color to use for each of the bitmap's “1” valued
          pixels in its normal, active and disabled states (correspondingly).
          The given value may be any valid :ref:`Tk colour <colours>`.

        | *state=*
        | This allows the bitmap to override the canvas widget's global
          *state* option. It takes the same values: normal, disabled or
          hidden. An empty string will defer to the canvas widget's state.
          The default value is an empty string.

        | *tags=*
        | Specifies one or more tags to apply to the bitmap. When used in
          :mod:`Canvas.itemconfigure`, this replaces any existing tags for the
          bitmap. An empty list may also be specified. The default value is an
          empty list.

    .. method:: create_image(*args, **kw)

    .. method:: create_line(*args, **kw)

    .. method:: create_oval(*args, **kw)

    .. method:: create_polygon(*args, **kw)

    .. method:: create_rectangle(*args, **kw)

    .. method:: create_text(*args, **kw)

    .. method:: create_window(*args, **kw)

    .. method:: itemconfigure()


.. _coordinates:

Coordinates
-----------

TODO
