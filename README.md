基于二开pptxgenjs，扩展了 linearGradient、radialGradient、pathGradient 的支持。

## 使用示例

### linearGradient
```ts
const pptx = new PptxGenJS()
const slide = pptx.addSlide()

slide.addShape(pptx.ShapeType.rect, {
	x: 1, y: 1, w: 4, h: 2,
	fill: {
		type: 'linearGradient',
		angle: 45,
		stops: [
			{ position: 0, color: 'FF0000' },
			{ position: 100, color: '0000FF' }
		]
	}
})
```

### radialGradient
```ts
const pptx = new PptxGenJS()
const slide = pptx.addSlide()

slide.addShape(pptx.ShapeType.rect, {
	x: 1, y: 1, w: 4, h: 2,
	fill: {
		type: 'radialGradient',
		path: 'circle',
		stops: [
			{ position: 0, color: '00FF00' },
			{ position: 100, color: '0000FF' }
		]
	}
})
```

### pathGradient
```ts
const pptx = new PptxGenJS()
const slide = pptx.addSlide()

slide.addShape(pptx.ShapeType.rect, {
	x: 1, y: 1, w: 4, h: 2,
	fill: {
		type: 'pathGradient',
		path: 'shape',
		fillToRect: { t: 10, r: 10, b: 10, l: 10 },
		stops: [
			{ position: 0, color: 'FFFFFF' },
			{ position: 100, color: 'FF8800' }
		]
	}
})
```