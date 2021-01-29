There are two types of action link in mvc
1. First for you can show only **icon**
```
<a href="@Url.Action("List", "Home")" class="btn btn-info"> Cancel </a>
```
2. Second for **text** only
```
@Html.ActionLink("Cancel", "List", "Home", null, new { @class = "btn btn-danger" })
```
