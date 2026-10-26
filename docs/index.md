---
title: Translations of W3C standards and notes
description: List of translated W3C standards and notes (authorized and volunteer translations)
feed: https://www.w3.org/translations/feed/
---
{% include custom_css.html %}
<p class="lead">W3C supports volunteers who translate web standards into their language.</p>

<p>This page lists authorized and volunteer translations of <a href="https://www.w3.org/TR/">current W3C standards and notes</a>. In case of disputes, the authoritative version of the specification is the original, English document.</p>

<p><strong>Help make W3C standards available in your language:</strong> See <a href="/translations/contribute/">Contributing to W3C translations</a>.</p>

<nav class="l-cluster">
    <ul class="clean-list">
        <li><a href="authorized/">View authorized translations only</a></li>
        <li><a href="historical/">View translations of historical reports</a></li>
    </ul>
</nav>

<div class="translations-list">
{%- assign exceptions = "s-WCAG22, s-WCAG21" -%}
{%- assign cfts = site.data.translations | where_exp:"item", "item.countPublishedTranslations > 0" | where_exp:"item","item.isLatest == true or exceptions contains item.id" -%}
{%- for cft in cfts -%}
    {% include spec-listing.html filter="published" %}
{%- endfor %}
</div>

<div class="l-box l-box--no-border l-box--no-padding">
	<div class="pre-footer">
		<div class="l-switcher">
			<div>
				<div>
					<h2 class="h4">Related RSS feed</h2>
                    <div class="with-icon--before with-icon--larger">
                            <img class="icon icon--larger" src="https://www.w3.org/assets/website-2021/svg/rss.svg" width="30" height="30" alt="" aria-hidden="true">
                            <a href="{{page.feed}}">Recently published translations</a>
                        </div>
				</div>
		    </div>
	    </div>
    </div>
</div>