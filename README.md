# React and D3 JS Sandbox

**Mac OS Showstopper Buster**
sudo chown -R $USER /usr/local/lib/node_modules

**Framework and Library**

Basic HTML React Render 

"""
React.render(
    React.createElement(H1BGraph,{url:"data/h1bs.csv"}),
    document.querySelectorAll('.h1bgraph')[0]
);
"""

React Render with JSX 

"""
React.render(
    <H1BGraph url="data/h1bs.csv"/>,
    document.querySelectorAll('.h1bgraph')[0]
);
"""

**Approach**
* React owns the DOM
* d3 owns properties 

React

"""
render: function(){
    return(
        <g transform="translate(50,20)">
            <rect width="100" height="200"/>
        </g>
    );
}
"""

d3

"""
d3.select("svg")
  .append("g")
  .attr("transform","translate(50,20)")
  .append("rect")
  .attr("width",100)
  .attr("height",200);

"""

