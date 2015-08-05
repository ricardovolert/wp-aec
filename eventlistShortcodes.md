# Eventlist Shortcode Display Options #
_Shortcode options are listed in the following format_
<br><b>option</b> = "sample value" <code>[</code> valid inputs <code>]</code> <b>defaults are listed in bold</b>

<b>categories</b> = "1,2,3" <code>[</code> one or more comma separated category ids <code>]</code> <b>all categories are displayed when undefined</b> <br>Display only events associated with listed <a href='#Category_IDs.md'>category ids*</a>

<b>excluded</b> = true <code>[</code> <b>false</b> | true <code>]</code> <br>Display only events NOT associated with categories listed in the categories parameter<br>
<br>
<b>Tip</b>: <i>Consider using the <b>excluded</b> parameter if your setups has many categories and you only want to omit a few categories - it can mean less typing, and has the added benefit of automatically including any newly created categories without making changes to the shortcode parameters.</i>

<b>start</b> = "2011-07-10" <code>[</code> "<b>today</b>" | <a href='#Available_Date_Inputs.md'>Available Date Inputs</a> <code>]</code> <br>Display events starting on or after the specified date<br>
<br>
<b>end</b> = "tomorrow" <code>[</code> <b>"+1 year"</b> | <a href='#Available_Date_Inputs.md'>Available Date Inputs</a> <code>]</code> <br>Display events ending on or before the specified date<br>
<br>
<b>limit</b> = 5 <code>[</code> <b>15</b> | integer <code>]</code> <br>Limit events displayed to the specified integer<br>
<br>
<b>whitelabel</b> = true <code>[</code> <b>false</b> | true <code>]</code> <br>Display events without colors<br>
<br>
<b>reverse</b> = false <code>[</code> <b>false</b> | true <code>]</code> <br>Display events in reverse order<br>
<br>
<b>noresults</b> = "Nada" <code>[</code> <b>"No Upcoming Events"</b> | text <code>]</code> <br>Display specified text when no events are returned<br>
<br>
<h1>Available Date Inputs</h1>
<ol><li>YYYY-MM-DD<br>
<ul><li>2010-10-10<br>
</li><li>2011-01-01<br>
</li></ul></li><li>next | last | today | tomorrow | yesterday | week | month | year<br>
<ul><li>today<br>
</li><li>tomorrow<br>
</li><li>yesterday<br>
</li><li>last week<br>
</li><li>next month<br>
</li><li>last year<br>
</li></ul></li><li>(+/-) integer <code>[</code> days | weeks | months | years <code>]</code>
<ul><li>+3 days (three days from current date)<br>
</li><li>+2 weeks  (two weeks from current date)<br>
</li><li>-2 months (two months prior to current date)<br>
</li><li>-3 years (three years prior to current date)</li></ul></li></ol>

<h1>Examples</h1>
<ol><li>Display category id 3 only, beginning March 1, 2012, ending March 7, 2012<br>
<pre><code>[eventlist categories=1,2,4 start="2012-03-01" end="2012-03-07"]<br>
</code></pre>
</li><li>Assuming a setup with category ids 1, 2, 3 and 4; this shortcode produces the same result as the previous shortcode by using the <b>excluded</b> parameter.<br>
<pre><code>[eventlist categories=3 excluded=true start="2012-03-01" end="2012-03-07"]<br>
</code></pre>
</li><li>Display category ids 1, 2 and 4, beginning in the last 7 days, ending today (default), listed in reverse order, limited to the last 10 events<br>
<pre><code>[eventlist categories="1,2,4" start="last week" limit=10 reverse=true]<br>
</code></pre></li></ol>

<h1>Category IDs</h1>
Category ids are listed on the plugin's Manage Categories page<br>
<img src='http://dl.dropbox.com/u/6059938/manage%20categories.png' />