# 欢迎来到 MATT 的主页

# 前排提醒

如果访问慢的同学可以去[这个网站](https://1.1.1.1)下载软件

能正常访问[测试网站](https://www.youtube.com)即算成功

# C++公益优化项目（请自取）

1、火车头（感谢：胥寻之）

（慎用，只有在Win中有效，例如Hydrojudge，LG过不了）

```cpp
#pragma GCC optimize(1)
#pragma GCC optimize(2)
#pragma GCC optimize(3)
#pragma GCC optimize("Ofast")
#pragma GCC optimize("inline")
#pragma GCC optimize("-fgcse")
#pragma GCC optimize("-fgcse-lm")
#pragma GCC optimize("-fipa-sra")
#pragma GCC optimize("-ftree-pre")
#pragma GCC optimize("-ftree-vrp")
#pragma GCC optimize("-fpeephole2")
#pragma GCC optimize("-ffast-math")
#pragma GCC optimize("-fsched-spec")
#pragma GCC optimize("unroll-loops")
#pragma GCC optimize("-falign-jumps")
#pragma GCC optimize("-falign-loops")
#pragma GCC optimize("-falign-labels")
#pragma GCC optimize("-fdevirtualize")
#pragma GCC optimize("-fcaller-saves")
#pragma GCC optimize("-fcrossjumping")
#pragma GCC optimize("-fthread-jumps")
#pragma GCC optimize("-funroll-loops")
#pragma GCC optimize("-freorder-blocks")
#pragma GCC optimize("-fschedule-insns")
#pragma GCC optimize("inline-functions")
#pragma GCC optimize("-ftree-tail-merge")
#pragma GCC optimize("-fschedule-insns2")
#pragma GCC optimize("-fstrict-aliasing")
#pragma GCC optimize("-falign-functions")
#pragma GCC optimize("-fcse-follow-jumps")
#pragma GCC optimize("-fsched-interblock")
#pragma GCC optimize("-fpartial-inlining")
#pragma GCC optimize("no-stack-protector")
#pragma GCC optimize("-freorder-functions")
#pragma GCC optimize("-findirect-inlining")
#pragma GCC optimize("-fhoist-adjacent-loads")
#pragma GCC optimize("-frerun-cse-after-loop")
#pragma GCC optimize("inline-small-functions")
#pragma GCC optimize("-finline-small-functions")
#pragma GCC optimize("-ftree-switch-conversion")
#pragma GCC optimize("-foptimize-sibling-calls")
#pragma GCC optimize("-fexpensive-optimizations")
#pragma GCC optimize("inline-functions-called-once")
#pragma GCC optimize("-fdelete-null-pointer-checks")
```

2、数据类型定义（感谢：孙言龙）

```cpp
#define ll long long
#define ull unsigned ll
#define ld long double
#define mii map<int, int>
#define mll map<ll, ll>
#define mib map<int, bool>
#define mlb map<ll, bool>
#define mis map<int, string>
#define msi map<string, int>
#define si set<int>
#define sl set<ll>
#define pii pair<int, int>
#define pll pair<ll, ll>
#define psi pair<string, int>
#define pis pair<int, string>
#define csi const int
#define csl const ll
#define vct vector
#define mkp make_pair
#define fir first
#define sec second
#define vct vector
#define mst0(s) memset(s, 0, sizeof s)
#define mstinf(s) memset(s, 0x3f, sizeof s)
#define mstfinf(s) memset(s, 0xC0, sizeof s)
#define lowbit(u) ((u) & -(u))
```

3、自己手写的堆模板

```cpp
template <typename T>
struct Heap {
	vector<T> a;
	function<bool (T, T)> cmp;
	Heap(function<bool (T, T)> _c = [](T a, T b){ return a < b; }): cmp(_c) {
		a.resize(1);
	}
	inline auto size() {
		return a.size() - 1;
	}
	inline bool empty() {
		return size() == 0;
	}
	void push_up(int cur) {
		int nxt = cur >> 1;
		T dat = a[cur];
		while (nxt >= 1) {
			if (!cmp(a[nxt], dat)) break;
			a[cur] = a[nxt], cur = nxt, nxt >>= 1;
		}
		a[cur] = dat;
	}
	void push_down(int cur) {
		int nxt = cur << 1;
		T dat = a[cur];
		while (nxt <= size()) {
			if (nxt < size() && cmp(a[nxt], a[nxt + 1])) ++nxt;
			if (!cmp(dat, a[nxt])) break;
			a[cur] = a[nxt], cur = nxt, nxt <<= 1;
		}
		a[cur] = dat;
	}
	void push(T dat) {
		a.push_back(dat);
		push_up(size());
	}
	T top() {
		return a[1];
	}
	T pop() {
		T ret = a[1];
		swap(a[1], a[size()]);
		a.erase(a.begin() + size());
		push_down(1);
		return ret;
	}
};
```

说明：性质与`priority_queue`相似，小根堆传大于号，大根堆传小于号，使用`vector`存储，默认大根堆

<hr>

[三体笑话已转移](https://matthew101130.github.io/three-body-jokes/)

<hr>



<hr>



<hr>

知道<a href="https://www.vmware.com/go/tryworkstation-win-cn">VMware WorkStation Pro 17</a>吗？

<a href="https://www.vmware.com/go/getworkstation-win">Windows下载</a>


<a href="https://www.vmware.com/go/getworkstation-linux">Linux下载</a>

Win密钥：
```
MC60H-DWHD5-H80U9-6V85M-8280D
```
