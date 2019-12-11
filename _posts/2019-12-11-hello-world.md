---
layout: post
title: hello world
tags: [test, sample]
---
### 206 链表反转 99.25%

```js
function ListNode(val) {
	this.val = val;
	this.next = null;
}

var reverseList = function(head) {
	let pre = null, n = null
	while(head){
		n = head.next
		head.next = pre
		pre = head
		head = n
	}
	return pre
};

let l1 = new ListNode(1)
let l2 = new ListNode(2)
let l3 = new ListNode(3)
let l4 = new ListNode(4)
let l5 = new ListNode(5)
l1.next = l2
l2.next = l3
l3.next = l4
l4.next = l5

let n = reverseList(l1)
while(n){
	console.log(n.val)
	n = n.next
}
```

![img](images/nichijo0407.jpg)