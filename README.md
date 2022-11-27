# hmm

```javascript

function ec_(str) {
    const s = str.split('');
    let e = "";
    let e0 = "";
    let e1 = "";
    for (let i = 0;i < s.length;i++) {
    	e += s[i].replace("%","@D")+"%";
    }
    const w = e.split('');
    for (let n = 0;n < w.length;n++) {
    	e0 += w[n].replace("a","$r_")+"a";
    } 
    const rc = e0.split('');
    for (let n = 0;n < rc.length;n++) {
    	e1 += rc[n].replace("b","$rx_")+"b";
    } 
    return e1;

    
}
function de_(str) {
	const s = str.split('b');
	let e =  "";
	let e0 = "";
	let e1 = "";
	for (let i = 0;i < s.length;i++) {
		e += s[i].replace("$rx_","b");
	}
	const v = e.split('a');
	for (let i = 0;i < v.length;i++) {
		e0 += v[i].replace("$r_","a");
	}
	const u = e0.split('%');
	for (var i = 0; i < u.length; i++) {
		e1 += u[i].replace("@D","%");
	}
	return e1;
}


```
