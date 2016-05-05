# react-redux-explained

(a naive explanaition for myself during learning these things)

## Application root

As in any application using a database, on the initialization part of it you'll make the connection, usually by selecting the schema, too, in case we consider that we can connect to whole database.

In the first part presented below it is a simple relation, usually found in all React/Redux examples, but, I found that, if you want to build a more flexible application - as ex using React Native, too - it's a bit better to use the second.  

![App](img/App.png "Application start")  
  
## Redux

Redux represents more a document database, but, for the sake of simplicity I draw it and explained as a relational database, as seen below. Using a unique store is quite enough, you can justify a second store only if you have to separate applications in the same project.
 
Also, the levels presented here are flexible and orientative, you can add/remove as many levels and Reducers as you want on any branch. Shown is just convention for comparison.  

![Redux](img/Redux.png "Redux structure") 

## RRMVC

One of the definitions of MVC architecture is shown as below:

<!--![MVC](img/ocEWx.png)-->
<img src="img/ocEWx.png" width=400 />

That's why, in a simplified model React/Redux can be represented in the same way:

![RRMVC](img/RRMVC.png "RRMVC")


## Stacking

Stacking the Components/Containers is possible in 2 ways. 

The 3rd representation probably, not yet experimented, I don't know if is over-engineering. Probably gives some flexibility with the cost of extra code.   

![Stacking](img/Structure.png "Stacking")

Trying to figure out what would be interesting to use I realized that: 

First way is the way of a React only stacking, a normal way to stack dumb components without implying Redux. Absolutely the way to go if you want a separation of elements displayed in the page. 

Second way is specific to Redux way of stacking, the main issue with that is that you have to import stuff between containers and components and, at a certain point, it becomes difficult to follow the structure. Going back and forth between containers and components can give some confusion when, sometimes, you're naming the file in the same way.
 
### 3rd way thoughts
 
Third way is probably a better way in having only one fashion to require things. Components can import only components (first model), containers can import only a component (a container that represent that component) or only containers (pass child containers to parent container). Result is boilerplating. It worth it? How do we pass a container to a component? 

Now we have "component containers" and "layout containers". Damn, it's becoming overkill.

One way could be by using `this.props.children`, not so sure is very likeable. 

```
    var Wrap = React.createClass({
        render: function() {
            return <div>{ this.props.children }</div>;
        }
    });
    
    var App = React.createClass({
        render: function() {
            return <Wrap><h1>Hello word</h1></Wrap>;
        }
    });
```

A better way (in my opinion, lets see if feasible) is to pass containers through props, and define them into contract as `React.PropTypes.element`.


## Application organisation / Project structure 

Kind of difficult to chose, depends on the size of the project. I would chose a more complex one even for a simple project.

http://engineering.kapost.com/2016/01/organizing-large-react-applications/

http://jaysoo.ca/2016/02/28/organizing-redux-application/

http://marmelab.com/blog/2015/12/17/react-directory-structure.html

