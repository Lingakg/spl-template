# super pipeline

```typescript
import Pipe from 'super-pipeline';

const tool = new Pipe(__dirname, '/.pipe/main.yaml')
tool.getList()
const myConsole = tool.getInstance('console')

myConsole.tap.onTap('willStart', (data: any, context: any)=>{
  context.util.log.info('program',data)
})


myConsole.tap.emit('willStart', 'test')


myConsole.run()

```