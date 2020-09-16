
# YAROKHIN KIRYL

## CONTACTS

* **Phone**: +375 (29) 926-70-64
* **Email**: erokhinkirill@gmail.com
* **Github**: <https://github.com/ErKir>

## SUMMARY

I want to become a JavaScript engineer. I would like to gain technical skills and knowledge of front-end & back-end development to create high quality products. I am constantly learning new knowledge, I am persistent, and able to learn and achieve my goals. I try to keep abreast of new trends in IT.

## KEY SKILLS

Basic knowledge: **JS** (ES6), **Babel**, **SQL**, **Git**, **HTML**, **CSS**, **Linux shell**.

## CODE EXAMPLES

***sortDeps.js*** - takes a list of dependencies as input and returns a list (array) of sorted nodes. <https://ru.hexlet.io/code_reviews/124789>

Dependency management is a very important task in software development. Applications typically involve many third-party components, which in turn may also rely on third-party components. One of the tasks of a dependency manager is to include dependencies in the correct order. Libraries that others depend on should link earlier. The definition of this sequence is reduced to the task of sorting the graph.

``` js script

export default (deps) => {
    const add = (acc, node) => {
        const subDeps = deps[node] || [];
        const subAcc = subDeps.reduce(add, []);
        return { ...acc, ...subAcc, [node]: true };
    };
    const set = Object.keys(deps).reduce(add, {});
    return Object.keys(set);
};

```

***convert.js*** is a function that takes an array of a certain structure as input and returns an object obtained from this array.
<https://ru.hexlet.io/code_reviews/123794>

The array is designed in such a way that it can be used to represent associative arrays. Each value inside it is an array of two elements, where the first element is the key and the second is the value. In turn, if the value is also an array, then it is considered to be a nested representation of the associative array. In other words, any array within the original array is always considered data to be converted to an object.

```js script

const convert = arr => arr.reduce((acc, element) => {
    if (Array.isArray(element)) {
        const [key, value] = element;
        return Array.isArray(value) ? { ...acc, [key]: convert(value) } :
        { ...acc, [key]: value };
    }
    return acc;
}, {});

export default convert;

```

## EDUCATION

Hexlet programming courses: Node.js programmer
<https://ru.hexlet.io/u/userk>

## ENGLISH LEVEL

The level of English is basic (between A2 - A1). I can build short simple sentences, I understand the context of not fast speech. I read technical documentation almost without using a dictionary. *Duolingo is following me, it's everywhere*.
