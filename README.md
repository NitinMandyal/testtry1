# testtry1
from limited internet access

Selenium.prototype.doTypeCaptcha = function(locator,text) {

var element = this.page().findElement(locator);

var ans=0;

var i=0;

var j=0;

var num = text.match(/\d+/g);

var oper= text.length – num.length;

for(var i=0;i<num.length;i++)

{

num[i]=parseInt(num[i],10);

}

ans=num[0];

for (i=1;i<=oper;i++)

{

for(;j<text.length;j++)

{

if(text[j]==”+” || text[j]==”-” || text[j]==”*” || text[j]==”/”)

{

break;

}

}

if(text[j]==”+”)

{

ans=ans+num[i];

}

if(text[j]==”-“)

{

ans=ans-num[i];

}

if(text[j]==”*”)

{

ans=ans*num[i];

}

if(text[j]==”/”)

{

ans=ans/num[i];

}

j=j+1;

}

this.page().replaceText(element,ans);

<!—the above statement will put ‘ans’ value in the required element–>

}; // End of the file
