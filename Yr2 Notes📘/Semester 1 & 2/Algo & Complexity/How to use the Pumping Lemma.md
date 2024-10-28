# How to use the Pumping Lemma
---
> [!info]+ File Details
> Includes information about this (genus:: Note) from [Year::2]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  28-10-2024
> > *Module :* [[Algorithms and Complexity]]
> > *Teacher*: 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> > [[#Speed run]]
> [[#]]
> [[#]]
> [[#]]
> [[#]]

--- 
> [!danger]+ *Speed run*
> Break down of topic 
> > $a)$ -  
> $b)$ - 
> $c)$ - 

---

### About the pumping lemma
[[Pumping Lemma]]

### Summary

In any regular language there is a number $n$, called the pumping length, such that all words in $L$ of $length ≥ n$ can be “pumped”. How to prove that a language $L$ is not regular:
1. Suppose that $L$ is regular. 
2. Then by the pumping lemma, all words that are sufficiently big can be pumped. 
3. Show that for any $n$, there is some word $w ∈ L$ of $length ≥ n$ that cannot be pumped. 
4. Contradiction! 
5. Therefore our original claim was false, and $L$ cannot be regular


### Proof

1. Suppose $L$ is regular. Then by the pumping lemma there exists some $n \gt 0$ such that all words w with $|w| \geq n$ can be pumped 
2. Make a clever choice of $w ∈ L$ with $|w| ≥ n$. Your choice will need to work for any possible value of $n$. 
	Define $w = 0^n1^n \in L$, and note that $|w| = 2n \geq n$.
3. By the pumping lemma there is some division $w = xyz$ with 
> $y=e$  
> $|xy| ≤ n$
> $xy^iz ∈ L$ for $i ≥ 0$ 
4. For any such division, try to use the fact that $y= e$ and $|xy| ≤ n$ to find some $i ≥ 0$ such that $xy^iz / ∈ L$.
5.  You will have then found a CONTRADICTION, therefore L is not regular


### Common mistakes

Let $n = 4$, $w=0^41^4$

what the hell $$\begin{align} \text{Let} w = 0^n1^n\\...\text{Let} x = e, y = 0^m, z=1^n \\\end{align}$$


### Examples

![[pumping lemma ex1.png|500]]


## Use of the lemma to prove non-regularity

[[edit](https://en.wikipedia.org/w/index.php?title=Pumping_lemma_for_regular_languages&action=edit&section=2 "Edit section: Use of the lemma to prove non-regularity")]

The pumping lemma is often used to prove that a particular language is non-regular: a [proof by contradiction](https://en.wikipedia.org/wiki/Proof_by_contradiction "Proof by contradiction") may consist of exhibiting a string (of the required length) in the language that lacks the property outlined in the pumping lemma.

> Example: The language L={anbn:n≥0}![{\displaystyle L=\{a^{n}b^{n}:n\geq 0\}}](https://wikimedia.org/api/rest_v1/media/math/render/svg/d04a0afeb79718d60e0b5b08f147a0b489297a5f) over the alphabet Σ={a,b}![{\displaystyle \Sigma =\{a,b\}}](https://wikimedia.org/api/rest_v1/media/math/render/svg/255f4d881839df215d854245ff316beb7c7e67b5) can be shown to be non-regular as follows:
> 
> 1. Let w,x,y,z![{\displaystyle w,x,y,z}](https://wikimedia.org/api/rest_v1/media/math/render/svg/d0f4eccb8967a0d5b5c01afd77c7cfc33a61330f), and n![{\displaystyle n}](https://wikimedia.org/api/rest_v1/media/math/render/svg/a601995d55609f2d9f5e233e36fbe9ea26011b3b) be as used in the [formal statement for the pumping lemma](https://en.wikipedia.org/wiki/Pumping_lemma_for_regular_languages#Formal_statement) above.
> 2. Assume that some constant p![{\displaystyle p}](https://wikimedia.org/api/rest_v1/media/math/render/svg/81eac1e205430d1f40810df36a0edffdc367af36) exists as required by the lemma.
> 3. Let w![{\displaystyle w}](https://wikimedia.org/api/rest_v1/media/math/render/svg/88b1e0c8e1be5ebe69d18a8010676fa42d7961e6) in L![{\displaystyle L}](https://wikimedia.org/api/rest_v1/media/math/render/svg/103168b86f781fe6e9a4a87b8ea1cebe0ad4ede8) be given by w=apbp![{\displaystyle w=a^{p}b^{p}}](https://wikimedia.org/api/rest_v1/media/math/render/svg/25dfd6c22fa59f94893c9d51126379c05ef2bd7e), which is a string longer than p![{\displaystyle p}](https://wikimedia.org/api/rest_v1/media/math/render/svg/81eac1e205430d1f40810df36a0edffdc367af36).
> 4. By the pumping lemma, there must exist a decomposition w=xyz![{\displaystyle w=xyz}](https://wikimedia.org/api/rest_v1/media/math/render/svg/8836e20eb4df474ea3a76120b8bfcb4c3f79f25f) with |xy|≤p![{\displaystyle |xy|\leq p}](https://wikimedia.org/api/rest_v1/media/math/render/svg/c2cf6670a2d20395afdc1fa18ed8935ecb980a54) and |y|≥1![{\displaystyle |y|\geq 1}](https://wikimedia.org/api/rest_v1/media/math/render/svg/e949835f150dfe886776296b912457c704c17697) such that xyiz![{\displaystyle xy^{i}z}](https://wikimedia.org/api/rest_v1/media/math/render/svg/005170bde2715799ae793824f59dddd63013227d) in L![{\displaystyle L}](https://wikimedia.org/api/rest_v1/media/math/render/svg/103168b86f781fe6e9a4a87b8ea1cebe0ad4ede8) for every i≥0![{\displaystyle i\geq 0}](https://wikimedia.org/api/rest_v1/media/math/render/svg/405e1424cb9c4fc171c433a8e8f04b3e5938e366).
> 5. Since |xy|≤p![{\displaystyle |xy|\leq p}](https://wikimedia.org/api/rest_v1/media/math/render/svg/c2cf6670a2d20395afdc1fa18ed8935ecb980a54), the string y![{\displaystyle y}](https://wikimedia.org/api/rest_v1/media/math/render/svg/b8a6208ec717213d4317e666f1ae872e00620a0d) only consists of instances of a![{\displaystyle a}](https://wikimedia.org/api/rest_v1/media/math/render/svg/ffd2487510aa438433a2579450ab2b3d557e5edc).
> 6. Because |y|≥1![{\displaystyle |y|\geq 1}](https://wikimedia.org/api/rest_v1/media/math/render/svg/e949835f150dfe886776296b912457c704c17697), it contains at least one instance of the letter a![{\displaystyle a}](https://wikimedia.org/api/rest_v1/media/math/render/svg/ffd2487510aa438433a2579450ab2b3d557e5edc).
> 7. Pumping y![{\displaystyle y}](https://wikimedia.org/api/rest_v1/media/math/render/svg/b8a6208ec717213d4317e666f1ae872e00620a0d) to give xy2z![{\displaystyle xy^{2}z}](https://wikimedia.org/api/rest_v1/media/math/render/svg/735b8fd75e204d8b628a07e13e0c15acfc898f8b) gives a word with more instances of the letter a![{\displaystyle a}](https://wikimedia.org/api/rest_v1/media/math/render/svg/ffd2487510aa438433a2579450ab2b3d557e5edc) than the letter b![{\displaystyle b}](https://wikimedia.org/api/rest_v1/media/math/render/svg/f11423fbb2e967f986e36804a8ae4271734917c3), since some instances of a![{\displaystyle a}](https://wikimedia.org/api/rest_v1/media/math/render/svg/ffd2487510aa438433a2579450ab2b3d557e5edc) but none of b![{\displaystyle b}](https://wikimedia.org/api/rest_v1/media/math/render/svg/f11423fbb2e967f986e36804a8ae4271734917c3) were added.
> 8. Therefore, xy2z![{\displaystyle xy^{2}z}](https://wikimedia.org/api/rest_v1/media/math/render/svg/735b8fd75e204d8b628a07e13e0c15acfc898f8b) is not in L![{\displaystyle L}](https://wikimedia.org/api/rest_v1/media/math/render/svg/103168b86f781fe6e9a4a87b8ea1cebe0ad4ede8) which contradicts the pumping lemma.
> 9. Therefore, L![{\displaystyle L}](https://wikimedia.org/api/rest_v1/media/math/render/svg/103168b86f781fe6e9a4a87b8ea1cebe0ad4ede8) cannot be regular.

![[pumping lemma ex2.png]]