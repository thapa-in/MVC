using(Html.BeginForm("Delete", "Employee", new{id=item.ID}))
{
<input type="submit" value="Delete" onclick="retrun confirm('Are you delete @item.id')"

}
