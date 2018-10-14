## Building with Serverless


<div>
  <div style="float: left; width:32%; align: center; padding:5px"><img src="images/stream.jpg"></img></div>
  <div class="fragment" style="float: left; width:32%; align: center; padding:5px">
    <a title="By Apfenn1, from Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Elmer%27s_Glue-All_historic_packaging.JPG"><img width="200" alt="Elmer&#039;s Glue-All historic packaging" src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/92/Elmer%27s_Glue-All_historic_packaging.JPG/256px-Elmer%27s_Glue-All_historic_packaging.JPG"></a>
    <div><font size="1">By Apfenn1, from Wikimedia Commons</font></div>
  </div>
  <div style="float: left; width:32%; align: center; padding:5px">
    <img src="images/buckets.jpg"></img>
    <div><font size="1">By GinaD, from Wikimedia Commons</font></div>
  </div>
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
