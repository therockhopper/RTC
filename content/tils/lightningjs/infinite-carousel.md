---
title: "Infinite Carousel"
date: 2022-05-12T17:46:39-03:00
---

```
export class Row extends Component {
  private slides;
  private index = 0;
  private slideSize = SpotlightCard.width;
  private allowShift: boolean = true;
  private animationDuration: number = 0.5;
  private xOffset: number = 1920 * 0.1;

  set content(slides) {
    this.index = 0;
    this.slides = slides;

    this.children = [ { type: SpotlightCard, x: -this.slideSize * 2 + this.xOffset, content: this.slides[this.slides.length - 2] }, { type: SpotlightCard, x: -this.slideSize + this.xOffset, content: this.slides[this.slides.length - 1] }, { type: SpotlightCard, x: 0 + this.xOffset, content: this.slides[0] }, { type: SpotlightCard, x: this.slideSize + this.xOffset, content: this.slides[1] }, { type: SpotlightCard, x: this.slideSize * 2 + this.xOffset, content: this.slides[2] }
    ];
  }

  _handleUp() {
    this.signal('setViewPosition', 1);
    return false;
  }

  _handleDown() {
    this.signal('setViewPosition', 1);
    return false;
  }

  /**
   * +1 left
   * -1 right
   */
  shiftSlide(dir: number) {
    if (!this.allowShift) return;
    this.allowShift = false;
    this.index = (this.index + this.slides.length + dir) % this.slides.length;
    let incoming;
    if (dir < 0) {
      incoming = {
type: SpotlightCard,
      content: this.contentLeft,
      x: -this.slideSize * 3 + this.xOffset
      };
      // add to start
      this.children = [incoming, ...this.children];
    } else {
      incoming = {
type: SpotlightCard,
      content: this.contentRight,
      x: this.slideSize * 3 + this.xOffset
      };
      // add to end
      this.children = [...this.children, incoming];
    }

    if (dir < 0) {
      this.children = this.children.map(c => {
          c.smooth = {
x: [
c.x + this.slideSize,
{ duration: this.animationDuration, timingFunction: 'ease-in' }
]
};
return c;
});
} else {
  this.children = this.children.map(c => {
      c.smooth = {
x: [
c.x - this.slideSize,
{ duration: this.animationDuration, timingFunction: 'ease-in' }
]
};
return c;
});
}

setTimeout(() => {
    // Enable the slider
    this.allowShift = true;
    dir < 0 ? this.children.pop() : this.children.shift();
    }, this.animationDuration);
}

get contentLeft() {
  return this.slides[
    (this.index + this.slides.length - 2) % this.slides.length
  ];
}

get contentRight() {
  return this.slides[(this.index + 2) % this.slides.length];
}

_getFocused() {
  return this.tag('Center');
}

_handleRight() {
  this.shiftSlide(1);
}
_handleLeft() {
  this.shiftSlide(-1);
}
}
```
