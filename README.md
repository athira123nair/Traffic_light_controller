# Traffic_light_controller
Implementation of traffic light controller using Verilog
<h4>Specifications of traffic controller</h4>
<p>Highways roads are given higher priority than Country roads.So by default highway light is made green,country light is made red.
  If any vehicles in detected in country road,then highway light i made yellow after 3ns and then to red.The country road is made to green till there 
  is no vehicle detected in country road.This can be explained using state flow diagram</p>
 <table style="width:100%">
  <tr>
    <th>STATE</th>
    <th>HIGHWAY_LIGHT</th>
    <th>COUNTRY_LIGHT</th>
  </tr>
   <tr>
    <td>S0</td>
    <td>green</td>
    <td>red</td>
  </tr>
  <tr>
    <td>S1</td>
    <td>yellow</td>
    <td>red</td>
  </tr>
  <tr>
    <td>S2</td>
    <td>red</td>
    <td>red</td>
  </tr>
  <tr>
    <td>S3</td>
    <td>red</td>
    <td>green</td>
  </tr>
  <tr>
    <td>S4</td>
    <td>red</td>
    <td>yellow</td>
  </tr>
  </table>
  <p>If x is high,then S0 to S4 happens and return to S0 if x becomes low</p>
<h4>Algorithm</h4>
<ol>
  <li>I have declared three inputs as</li>
    <ul>
      <li> clock</li>
      <li> reset</li>
      <li> x(a senor for detecting vehicles on country side)</li>
    </ul>
  <li>I have declared two outputs as</li>
   <ul>
      <li> highway_light</li>
      <li>country_light</li>
    </ul
     
  <li>To indicate the colour of light,it have given 2 bit binary using parameter</li>
  <li>Similary to indicate the state,I have used 3 bit binary using parameter</li>
  <li>If reset is high,then present state is low and if reset is low,then next state is assigned to present state</li>
  <li>states and there statments are declared using case statement</li>
</ol>
