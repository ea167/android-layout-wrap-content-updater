android-layout-wrap-content-updater
===================================

Update dynamically View sizes when layout_width or layout_height="wrap_content"


One of the annoying flaws of Android UI is its inability to update the size of Views defined with "wrap_content",
when we insert dynamically children views or when we modify their content.

This class is a workaround that recomputes sizes and forces a new layout for those views.

When invalidate(), requestLayout() or recomputeViewAttributes() don't work for you, 
simply call wrapContentAgain() on the view you want and it will reprocess all the subtree.


NOTES:
- This is not meant for high performance rendering, use it when your re-render your views every few seconds at most
- Must be called on UI-Thread (main thread), so post to a handler if needed
- To enable easier debugging, tag your nodes with android:tag="Name-of-my-node"
- Avoid using wrap_content on ScrollView!
- If you have center or right/bottom gravity, you should re-layout all nodes, not only the wrap_content: just call the method with the boolean set to true


End of nightmare, enjoy!

--Eric
