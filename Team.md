---
layout: page
title: Team
permalink: /tea/
---

We are recruiting!

<!--- markdown image without alignment
![bio_ShG](/assets/images/bio_ShG.jpg)
-->

<!--- markdown image with alignment
<img align="left" width="150" height="200" src="/assets/images/bio_ShG.jpg">
-->

<style>

  .flex-container {
    /* We first create a flex layout context */
    display: flex;
    
    /* Then we define the flow direction 
       and if we allow the items to wrap 
     * Remember this is the same as:
     * flex-direction: row;
     * flex-wrap: wrap;
     */
    flex-flow: row wrap;
    
    /* Then we define how is distributed the remaining space */
    justify-content: space-around;
    
    padding: 0;
    margin: 0;
    list-style: none;
  }

  .flex-item {
    display: flex;
    width: 500px;
    height: 400px;
    margin-top: 10px;
  }

/*  .container {
  display: flex;
  align-items: center;
  justify-content: center;
  }*/

  .img {
  width: 60px;
  }

  .text {
  font-size: 10px;
  padding-left: 10px;
  }
</style>

<body>

<div class="flex-container"
  <div class="flex-item">
    <div class="image">
      <img src="/assets/images/bio_ShG.jpg">
    </div>
    <div class="text">
      <h1>Shang Gao <br> Principal Investigator, <br> PhD, Univ. Geneva</h1>
    </div>
  </div>
</div>
</body>




[jekyll-organization]: https://github.com/jekyll
