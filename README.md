android-layout-wrap-content-updater
===================================

Update dynamically View sizes when layout_width or layout_height="wrap_content"


One of the annoying flaws of Android UI is its inability to update the size of Views defined with "wrap_content",
when we insert dynamically children views or when we modify their content.

This class is a workaround that recomputes sizes and forces a new layout for those views.

Simply call wrapContentAgain() on the view you want and it will reprocess all the subtree.


NOTES:
- This is not meant for high performance rendering, use it when your re-render your views every few seconds at most
- Must be called on UI-Thread (main thread), so post to a handler if needed
- To enable easier debugging, tag your nodes with android:tag="Name-of-my-node"
- Avoid using wrap_content on ScrollView!
- Works well with left and top gravity, but NOT yet with center (not tested with right / bottom)


End of nightmare, enjoy!

--Eric
