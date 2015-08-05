# Shortcode Options #

<br><i>Examples</i>
<br><code>[calendar categories="1,2,3" filter=2 month=8 views=false scroll=true]</code>
<br><code>[eventlist categories="1,2,3" excluded=true start="2011-09-01" end="+3 Weeks" limit=5 noresults="No Events Available"]</code>

<h3><code>[</code>calendar<code>]</code> and <code>[</code>eventlist<code>]</code> optional parameters</h3>

<b>categories</b> = "1,2,3" <code>[</code>one or more comma separated category ids<code>]</code> <br>defaults to <i>all categories</i> when unassigned<br>
<br>Display events from the specified category id(s)<br>
<br>
<b>excluded</b> = true <code>[</code>true<code>]</code>
<br>defaults to <i>false</i> when unassigned<br>
<br>Exclude categories listed in the categories parameter from being displayed<br>
<br>
<br>
<br>
<h3><code>[</code>calendar<code>]</code> only optional parameters</h3>

<b>filter</b> = 3 <code>[</code>integer | false<code>]</code>
<br>defaults to <i>all</i> when unassigned<br>
<br>Highlight the specified category id in the filter, and display only those events in the calendar - input <b>false</b> to hide the filter<br>
<br>
<b>view</b> = "basicDay" <code>[</code>basicDay | agendaDay | basicWeek | agendaWeek | month<code>]</code>
<br>defaults to <i>month</i> when unassigned<br>
<br>Display the specified calendar view<br>
<br>
<b>views</b> = "agendaDay, basicWeek" <code>[</code>one or more comma separated view labels | false <code>]</code>
<br>defaults to <i>"month,agendaWeek"</i> when unassigned<br>
<br>Display the specified view options in the calendar header - input <b>false</b> to hide the default view options<br>
<br>
<b>month</b> = 10 <code>[</code>integer<code>]</code>
<br>defaults to <i>current month</i> when unassigned<br>
<br>Display the specified calendar month on load<br>
<br>
<b>year</b> = 2001 <code>[</code>four digit integer<code>]</code>
<br>defaults to <i>current year</i> when unassigned<br>
<br>Display the specified calendar year on load<br>
<br>
<b>nav</b> = false <code>[</code>false<code>]</code>
<br>defaults to <i>true</i> when unassigned<br>
<br>Display calendar navigation buttons<br>
<br>
<b>scroll</b> = true <code>[</code>false<code>]</code>
<br>defaults to <i>false</i> when unassigned<br>
<br>Activate calendar mousewheel navigation<br>
<br>
<b>height</b> = 200 <code>[</code>integer<code>]</code>
<br>defaults to <i>automatic</i> when unassigned<br>
<br>Assign a minimum pixel height to the calendar<br>
<br>
<b>mini</b> = true <code>[</code>false<code>]</code>
<br>defaults to <i>false</i> when unassigned<br>
<br>Display the calendar as a minicalendar, displays nicely when applied within a sidebar or footer text widget<br>
<br>
<br>
<h3><code>[</code>eventlist<code>]</code> only  optional parameters</h3>

<b>start</b> = "2011-07-10" <code>[</code>date<code>]</code>
<br>defaults to <i>today</i> when unassigned<br>
<br>Display events starting on or after the specified date (yyyy-mm-dd date format required)<br>
<br>
<b>end</b> = "+2 Weeks" <code>[</code>date | <code>[</code>Day | Week | Month | Year<code>]</code> intervals<code>]</code>
<br>defaults to <i>"+1 Year"</i> when unassigned<br>
<br>Display events ending on or before the specified date or date interval (yyyy-mm-dd date format required)<br>
<br>
<b>limit</b> = 15 <code>[</code>integer<code>]</code>
<br>defaults to <i>4</i> when unassigned<br>
<br>Limit events displayed to the specified quantity<br>
<br>
<b>whitelabel</b> = true <code>[</code>true<code>]</code>
<br>defaults to <i>false</i> when unassigned<br>
<br>Render events without category colors<br>
<br>
<b>noresults</b> = "No Results" <code>[</code>text<code>]</code>
<br>defaults to <i>"No Upcoming Events"</i> when unassigned<br>
<br>Display this message when no events are returned