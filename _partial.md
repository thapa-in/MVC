#### Partial Action
1. Used like component
2. Make Action Method named "Gallery"
```C#
[ChildActionOnly]
public ActionResult Gallery()
{
    try
    {
        /* Get DATA : Async Api call */
        var syncContext = SynchronizationContext.Current;
        SynchronizationContext.SetSynchronizationContext(null);
        var modelData = infoRepo_.GetbyPageNoSectionNo(basicInfo_, 4).Result;
        SynchronizationContext.SetSynchronizationContext(syncContext);
        return PartialView("~/Views/_Gallery.cshtml", modelData);
    }
    catch (Exception ex)
    { return PartialView("_Gallery"); }
}
```
3. Create View with any name but add underscore before name 
    - It's not compulsary, but you can diffrenciate with-in views and partial view.
    - Replace code in it with model
4. Where ever you need to attach then call by Action name
```
@{ Html.RenderAction("PhotoGallery"); }
```


