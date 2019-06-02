# React RAWB Intersection Obeserver

If you want to have component react when they are in the viewport, this simple component helps you just do that.

## How to use

```javascript
import React from 'react';
import IntersectionObserver from 'react-rawb-intersection-observer';

class SuperCoolComponent extends React.Component {

    constructor (props, context) {
        super(props, context);
        this.state = {
            visible: false,
        };
    }

    visible () {
        this.setState({visible: true});
    }

    render () {
        return (
            <IntersectionObserver onVisible={this.visible.bind(this)} threshold={.5}>
                    { this.state.visible }
            </IntersectionObserver>
        );
    }

}

```



By wrapping you component with ```IntersectionObserver``` and giving a treshhold value (how much should be visible in the viewport in %), it will call the ```onVisible``` callback.

As simple as that.



