# React Responsive Image

Preserves aspect ratio space while loading in an image. Can be used with srcset and alt tags. Also can optionally show a loading animation.

Note: To preserve image space, the image will be styled as a block element.

## Installation

With Yarn:

```bash
yarn add react-responsive-img
```

Or with npm:

```bash
npm install --save react-responsive-img
```

## Usage

Basic usage:

```javascript
import Img from 'react-responsive-img'

const imageComponent = () => {
	<Img
		src='http://via.placeholder.com/500x1000'
		width={500}
		height={1000}
		alt={this.state.product.title}
		/>
}
```

With loading animation:

```javascript
import Img from 'react-responsive-img'
import LoadingAnimation from 'loading-animation'

const imageComponent = () => {
	<Img
		src='http://via.placeholder.com/500x1000'
		width={500}
		height={1000}
		loading={<LoadingAnimation />}
		/>
}
```

With srcset:

```javascript
import Img from 'react-responsive-img'
import LoadingAnimation from 'loading-animation'

const imageComponent = () => {
	<Img
		srcSet='
			http://via.placeholder.com/125x250 125w,
			http://via.placeholder.com/250x500 250w,
		'
		src='http://via.placeholder.com/500x1000'
		width={500}
		height={1000}
		/>
}
```
