# hmm

```javascript
/*
plain text encryption v1.0
make by: lê ngọc cương
carrd: lengoccuong.carrd.co
discord: https://discord.gg/WGckkSyupg
*/

//encode
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
//decode
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

# v2.0

```javascript

function encode(content) {
  const s = content.split('');
  let endToMiddle = "";
  let g = s.length;
  let result = "";
  /*làm ngược chuỗi */
  for (let i = 0;i < s.length;i++) {
      
      g = (g-1)
      endToMiddle += s[g];
  }
  /*thêm các ký tự ở char và char*/
  const a = endToMiddle.split('');
  let a01_ = "";
  for (let i = 0;i < a.length;i++) {
    a01_ += a[i].replace("@","%at")+"@";
  }
  const b = a01_.split('');
  let a02_ = "";
  for (let i = 0;i < b.length;i++) {
    a02_ += b[i].replace(".","%dt")+".";
  }
  const c = a02_.split('');
  let a03_ = "";
  for (let i = 0;i < c.length;i++) {
    a03_ += c[i].replace("~","%m")+"~";
  }
  result = a03_;
  return result;
}
function decode(content) {
const s = content.split('');
  let endToMiddle = "";
  let g = s.length;
  let result = "";
  /*làm ngược chuỗi */
  for (let i = 0;i < s.length;i++) {
      
      g = (g-1)
      endToMiddle += s[g];
  }
  /*chuyển đổi chuỗi đã được mã hóa thành chuỗi thường*/
  const ic = endToMiddle.split('~');
  let e = "";
  let e0 = "";
	let e1 = "";
	for (let i = 0;i < ic.length;i++) {
		e += ic[i].replace("%m","~");
	}
	const v = e.split('.');
	for (let i = 0;i < v.length;i++) {
		e0 += v[i].replace("td%",".");
	}
	const u = e0.split('@');
	for (var i = 0; i < u.length; i++) {
		e1 += u[i].replace("%at","@");
	}
  return e1;
}

```
