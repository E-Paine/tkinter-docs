*********************************
Commonly inherited widget methods
*********************************

.. class:: Widget

    A tkinter internal class inheriting common widget methods.

    .. method:: after(ms, func=None, *args)

    .. method:: after_cancel(id)

    .. method:: after_idle(func, *args)

    .. method:: anchor(anchor=None)

        See :mod:`Widget.grid_anchor`.

    .. method:: bell(displayof=0)

    .. method:: bind(sequence=None, func=None, add=None)

    .. method:: bind_all(sequence=None, func=None, add=None)

    .. method:: bind_class(className, sequence=None, func=None, add=None)

    .. method:: bindtags(tagList=None)

    .. method:: cget(key)

    .. method:: clipboard_append(string, **kw)

    .. method:: clipboard_clear(**kw)

    .. method:: clipboard_get(**kw)

    .. method:: columnconfigure(index, cnf={}, **kw)

        See :mod:`Widget.grid_columnconfigure`.

    .. method:: config(cnf=None, **kw)

        See :mod:`Widget.configure`.

    .. method:: configure(cnf=None, **kw)

    .. method:: deletecommand(name)

    .. method:: destroy()

    .. method:: event_add(virtual, *sequences)

    .. method:: event_delete(virtual, *sequences)

    .. method:: event_generate(sequence, **kw)

    .. method:: event_info(virtual=None)

    .. method:: focus_displayof()

    .. method:: focus_force()

    .. method:: focus_get()

    .. method:: focus_lastfor()

    .. method:: focus_set()

    .. method:: forget()

        See :mod:`Widget.pack_forget`.

    .. method:: getboolean(s)

    .. method:: getdouble(s)

    .. method:: getint(s)

    .. method:: getvar(name='PY_VAR')

    .. method:: grab_current()

    .. method:: grab_release()

    .. method:: grab_set()

    .. method:: grab_set_global()

    .. method:: grab_status()

    .. method:: grid(cnf={}, **kw)

        See :mod:`Widget.grid_configure`.

    .. method:: grid_anchor(anchor=None)

    .. method:: grid_bbox(column=None, row=None, col2=None, row2=None)

    .. method:: grid_configure(cnf={}, **kw)

    .. method:: grid_columnconfigure(index, cnf={}, **kw)

    .. method:: grid_forget()

    .. method:: grid_info()

    .. method:: grid_location(x, y)

    .. method:: grid_propagate(flag=['_noarg_'])

    .. method:: grid_remove()

    .. method:: grid_rowconfigure(index, cnf={}, **kw)

    .. method:: grid_size()

    .. method:: grid_slaves(row=None, column=None)

    .. method:: info()

        See :mod:`Widget.pack_info`.

    .. method:: image_names()

    .. method:: image_types()

    .. method:: keys()

    .. method:: location(x, y)

        See :mod:`Widget.grid_location`.

    .. method:: mainloop(n=0)

    .. method:: nametowidget(name)

    .. method:: option_add(pattern, value, priority=None)

    .. method:: option_clear()

    .. method:: option_get(name, className)

    .. method:: option_readfile(fileName, priority=None)

    .. method:: pack(cnf={}, **kw)

        See :mod:`Widget.pack_configure`.

    .. method:: pack_configure(cnf={}, **kw)

    .. method:: pack_forget()

    .. method:: pack_info()

    .. method:: pack_propagate(flag=['_noarg_'])

    .. method:: pack_slaves()

    .. method:: place(cnf={}, **kw)

        See :mod:`Widget.place_configure`.

    .. method:: place_configure(cnf={}, **kw)

    .. method:: place_forget()

    .. method:: place_info()

    .. method:: place_slaves()

    .. method:: propagate(flag=['_noarg_'])

        See :mod:`Widget.pack_propagate`.

    .. method:: quit()

    .. method:: register(func, subst=None, needcleanup=1)

    .. method:: rowconfigure(index, cnf={}, **kw)

        See :mod:`Widget.grid_rowconfigure`.

    .. method:: selection_clear(**kw)

    .. method:: selection_get(**kw)

    .. method:: selection_handle(command, **kw)

    .. method:: selection_own(**kw)

    .. method:: selection_own_get(**kw)

    .. method:: send(interp, cmd, *args)

    .. method:: setvar(name='PY_VAR', value='1')

    .. method:: size()

        See :mod:`Widget.grid_size`.

    .. method:: slaves()

        See :mod:`Widget.pack_slaves`.

    .. method:: tk_bisque()

    .. method:: tk_focusFollowsMouse()

    .. method:: tk_focusNext()

    .. method:: tk_focusPrev()

    .. method:: tk_setPalette(*args, **kw)

    .. method:: tk_strictMotif(boolean=None)

    .. method:: unbind(sequence, funcid=None)

    .. method:: unbind_all(sequence)

    .. method:: unbind_class(className, sequence)

    .. method:: update()

    .. method:: update_idletasks()

    .. method:: wait_variable(name='PY_VAR')

    .. method:: wait_visibility(window=None)

    .. method:: wait_window(window=None)

    .. method:: waitvar(name='PY_VAR')

        See :mod:`Widget.wait_variable`.

    .. method:: winfo_atom(name, displayof=0)

    .. method:: winfo_atomname(id, displayof=0)

    .. method:: winfo_cells()

    .. method:: winfo_children()

    .. method:: winfo_class()

    .. method:: winfo_colormapfull()

    .. method:: winfo_containing(rootX, rootY, displayof=0)

    .. method:: winfo_depth()

    .. method:: winfo_exists()

    .. method:: winfo_fpixels(number)

    .. method:: winfo_geometry()

    .. method:: winfo_height()

    .. method:: winfo_id()

    .. method:: winfo_interps(displayof=0)

    .. method:: winfo_ismapped()

    .. method:: winfo_manager()

    .. method:: winfo_name()

    .. method:: winfo_parent()

    .. method:: winfo_pathname(id, displayof=0)

    .. method:: winfo_pixels(number)

    .. method:: winfo_pointerx()

    .. method:: winfo_pointerxy()

    .. method:: winfo_pointery()

    .. method:: winfo_reqheight()

    .. method:: winfo_reqwidth()

    .. method:: winfo_rgb(color)

    .. method:: winfo_rootx()

    .. method:: winfo_rooty()

    .. method:: winfo_screen()

    .. method:: winfo_screencells()

    .. method:: winfo_screendepth()

    .. method:: winfo_screenheight()

    .. method:: winfo_screenmmheight()

    .. method:: winfo_screenmmwidth()

    .. method:: winfo_screenvisual()

    .. method:: winfo_screenwidth()

    .. method:: winfo_server()

    .. method:: winfo_toplevel()

    .. method:: winfo_viewable()

    .. method:: winfo_visual()

    .. method:: winfo_visualid()

    .. method:: winfo_visualsavailable(includeids=False)

    .. method:: winfo_vrootheight()

    .. method:: winfo_vrootwidth()

    .. method:: winfo_vrootx()

    .. method:: winfo_vrooty()

    .. method:: winfo_width()

    .. method:: winfo_x()

    .. method:: winfo_y()

.. class:: XView

    .. method:: xview(*args)

    .. method:: xview_moveto(fraction)

    .. method:: xview_scroll(number, what)

.. class:: YView

    .. method:: yview(*args)

    .. method:: yview_moveto(fraction)

    .. method:: yview_scroll(number, what)

