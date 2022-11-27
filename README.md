# hmm

```javascript

function ec_(e){let l=e.split(""),t="",r="",n="";for(let p=0;p<l.length;p++)t+=l[p].replace("%","@D")+"%";let a=t.split("");for(let c=0;c<a.length;c++)r+=a[c].replace("a","$r_")+"a";let f=r.split("");for(let i=0;i<f.length;i++)n+=f[i].replace("b","$rx_")+"b";return n}function de_(e){let l=e.split("b"),t="",r="",n="";for(let p=0;p<l.length;p++)t+=l[p].replace("$rx_","b");let a=t.split("a");for(let c=0;c<a.length;c++)r+=a[c].replace("$r_","a");let f=r.split("%");for(var i=0;i<f.length;i++)n+=f[i].replace("@D","%");return n}


```
