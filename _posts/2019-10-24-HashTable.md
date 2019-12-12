---
layout: post
title: Leetcode HashTable
tags: [leetcode, HashTable]
---

#### 242. 有效的字母异位词

```js
// 80ms 92.47%  38.3mb 34.88%
/**
 * @param {string} s
 * @param {string} t
 * @return {boolean}
 */
var isAnagram = function(s, t) {
	let a = [...Array(26)].map(_=>0)
	let b = [...Array(26)].map(_=>0)
	for (let i of s){
		a[i.charCodeAt()-97]++
	}
	for (let i of t){
		b[i.charCodeAt()-97]++
	}
	for (let i = 0; i < 26; i++){
		if (a[i] !== b[i]) return false
	}
	return true
};
```