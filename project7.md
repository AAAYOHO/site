#site
<style>
@keyframes fly
{
   from {height:700px}
    to{height:0px}
}
</style>
<script>
function Balloon(color1,diameter,speed)
{
    this . color = color;
    this . diameter = diameter;
    this . speed = speed;
    this .make= function()
    {

    }
    this . rise = function()
    {
           let  dv = document.createElement('div');
           dv . id = 'b' + this.id;
           dv.style.cssText = 'width:' + this . diameter +
'px;height' + diameter + 'px;border-radius:'+
(diameter/2) + 'px;background-color:' + this.color
+ ';position:absolute;left:' + (this.id*50) +
'px;top:700px';
            dv.innerHTML = '' +this.id;
           document.body.appendChild(dv);
    }
    this.rise = function()
   {
      let dv = document.getElementById('b' + this.id)
      dv.style.animationName = "fly";
      dv.style.animationDuration = ~~(700/this.speed) 
+ 's';  
 

   }    
}
let b = new Ballon(1,  'red',  200,  100); 
b.make();
b.rise();
