![textcircle-min](https://user-images.githubusercontent.com/83787591/220473583-28c40480-3942-4d15-90b6-ad7b0ab8723c.jpg)

# Astro Textcircle
If you want to showcase your text in a circular layout, give this Astro component a try.
> **While this component isn't inherently responsive, you can easily create multiple circles that adjust to fit the viewport - just keep this in mind.**


## [Live Demo](https://stackblitz.com/edit/withastro-astro-wu7yqp?file=src%2Fpages%2Findex.astro)


## Instalation
> using npm
```
npm install astro-textcircle
```
> using pnpm
```
pnpm add astro-textcircle
```


## Possible Props 
If Visual Studio Code is your preferred IDE, simply press CRTL+SPACE / CMD+SPACE to reveal the valid properties.
- **text** [sting]
- **class** [sting] 
- **options** [object]
- **animation** [object]

```js
interface Props {
	class?: string;
	text: string;
	options?: {
		spacing?: number;
		uppercase?: boolean;
		fontSizeInRem?: number;
		fontWeight?: 'lighter' | 'normal' | 'bold' | 'bolder' | number;
		divider?: string;
		dividerColor?: string;
		rotation?: number;
	};
	animation?: {
		duration: string;
		timing?: 'ease' | 'ease-in' | 'ease-out' | 'ease-in-out' | 'linear' | string;
		delay?: string;
		direction?: 'normal' | 'reverse';
		count?: 'infinite' | number;
		animateOnHover?: boolean;
		stopAnimateOnHover?: boolean;
	};
}
```

### **divider and dividerColor**
> Give your text a stylish twist with a divider instead of spacing - just use the **divider** property and set a custom color with **dividerColor**.
> 
> Keep in mind that in order to use the **dividerColor** property, the **divider** property must be set beforehand.

### **rotation**
> If the **rotation** of your text isn't to your liking, don't worry - simply adjust it with the rotate property. Just input a number in degrees and watch your text rotate accordingly.

### **animation**
> If you are using the **animation** property, you need to declare the **duration** poperty! 

### **animateOnHover**
> This property will start the animation on hover.

### **stopAnimateOnHover**
> This property will stop the animation on hover.
> 
> Keep in mind that using **animateOnHover** + **stopAnimateOnHover** will result in **animateOnHover**


## How to use
```js
---
import { Textcircle } from 'astro-textcircle';
---

<div>

  <!-- basic -->
  <Textcircle text="Display text in a circle" />

  <!-- using class with tailwind -->
  <Textcircle 
    text="Display text in a circle" 
    class="text-red-500 absolute top-8 left-8"
  />

  <!-- using options -->
  <Textcircle 
    text="Display text in a circle"
    options={{ 
      uppercase: true,
      fontSizeInRem: 0.75,
      fontWeight: 'bold',
      divider: '-',
      dividerColor: 'red',
      rotation: 45
    }}
  />

  <!-- using animation -->
  <Textcircle 
    text="Display text in a circle"
    animation={{ 
      duration: '12s',
      timing: 'linear',
      delay: '5s',
      direction: 'reverse',
      count: 'infinite',
      animateOnHover: true
    }}
  />

</div>
```
> Notice that every letter and spacing in your text will be outputed as **set:html={}** 