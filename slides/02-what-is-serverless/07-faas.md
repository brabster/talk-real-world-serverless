## Building with Serverless

<div class="fragment">
<a title="By Apfenn1 [CC BY-SA 4.0
 (https://creativecommons.org/licenses/by-sa/4.0
)], from Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Elmer%27s_Glue-All_historic_packaging.JPG"><img width="256" alt="Elmer&#039;s Glue-All historic packaging" src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/92/Elmer%27s_Glue-All_historic_packaging.JPG/256px-Elmer%27s_Glue-All_historic_packaging.JPG"></a>
<div><font size="1">By Apfenn1 [CC BY-SA 4.0(https://creativecommons.org/licenses/by-sa/4.0)], from Wikimedia Commons</font></div>
</div>

Note:
 - Given a bunch of serverless solutions, how do you assemble them into something that solves problems?
 - BaaS - pre-integrated
   - Firebase, 1Backend, Backendless
   - Suites of services that cover most/all common needs for apps, websites
   - Particularly good for frontend-strong teams
   - But make sure you understand the security model! https://www.bleepingcomputer.com/news/security/thousands-of-apps-leak-sensitive-data-via-misconfigured-firebase-backends/
 - Self-assembly
   - Need to connect other services together
   - eg transcoding video, thumbnailing, ml
   - ...so need servers?
   - thus FaaS
