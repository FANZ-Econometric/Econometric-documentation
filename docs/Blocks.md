<div class="col-2">
<h2>UI Suggestions</h2>
    <ul class="sub-menu">
        <li class="menu-item"><a href="UIstart">Basic Settings</a></li>
        <li class="menu-item"><a href="Blocks">Block Details</a></li>
        <li class="menu-item"><a href="Fertiliser">Fertiliser Details</a></li>
       <li class="menu-item"><a href="Enterprise">Enterprise Data</a></li>
       <li class="menu-item"><a href="Reports">Reports</a></li>
    </ul>
</div>
<div class="col-8">
        <h3>Block Details</h3>
        <p>For each block the following information is required:</p>
        <p>Soil test data, rainfall/drainage data, pasture intake (kg/DM/ha), fert spreading costs (including lime) sulphur history and RPR history.</p>
        <p>The options for soil group, soil order, topography, drainage, and reserve K level can be found here: <a href="https://github.com/FANZ-Econometric/Econometric-documentation/blob/main/schema/Model_Request_details.md">Model Request Details</a></p>
        <p>For soil - either use soil group or order, you don't need both.</p>
        <p>Options for entering other inputs or outputs such as supplements, fertiliser applied or effluent can be included however you want to capture it.</p>
        <p>Sulphur soil tests can be entered in one of three ways (in order of use):</p>
        <ul class="bullet">
          <li>Organic S</li>
          <li>Total S</li>
          <li>QTSO4</li>
          </ul>
          <p>If none are provided = 0 then a default of 10 is used.</p>
        <img src="images/blocks.png" alt="Blocks">
        <img src="images/blockadditional.png" alt="Blocks">
    <p>Fertiliser and Lime spreading costs are calculated for each block.</p>
    <img src="images/fertcalc.png" alt="fert calc">
    <img src="images/limecalc.png" alt="lime calc">
    </div>
