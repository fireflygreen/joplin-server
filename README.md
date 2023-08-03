# joplin-server
joplin server for android usage




deploy to a paas, using elephantSql: 
but issue with concurrent access , ruslin not good at this


```
 [error] App: Middleware error on /api/items/root:/070d8bfdf4grw656515ecd.md:/content: error: too many connections for role "postgresql"
Aug 2 10:23:06 PM      at Parser.parseErrorMessage (/home/joplin/packages/server/node_modules/pg-protocol/src/parser.ts:369:69)
Aug 2 10:23:06 PM      at Parser.handlePacket (/home/joplin/packages/server/node_modules/pg-protocol/src/parser.ts:188:21)
Aug 2 10:23:06 PM      at Parser.parse (/home/joplin/packages/server/node_modules/pg-protocol/src/parser.ts:103:30)
Aug 2 10:23:06 PM      at Socket.<anonymous> (/home/joplin/packages/server/node_modules/pg-protocol/src/index.ts:7:48)
Aug 2 10:23:06 PM      at Socket.emit (node:events:513:28)
Aug 2 10:23:06 PM      at addChunk (node:internal/streams/readable:324:12)
Aug 2 10:23:06 PM      at readableAddChunk (node:internal/streams/readable:297:9)
Aug 2 10:23:06 PM      at Socket.Readable.push (node:internal/streams/readable:234:10)
Aug 2 10:23:06 PM      at TCP.onStreamRead (node:internal/stream_base_commons:190:23) {
Aug 2 10:23:06 PM    length: 110,
Aug 2 10:23:06 PM    severity: 'FATAL',
Aug 2 10:23:06 PM    code: '53300',
Aug 2 10:23:06 PM    detail: undefined,
Aug 2 10:23:06 PM    hint: undefined,
Aug 2 10:23:06 PM    position: undefined,
Aug 2 10:23:06 PM    internalPosition: undefined,
Aug 2 10:23:06 PM    internalQuery: undefined,
Aug 2 10:23:06 PM    where: undefined,
Aug 2 10:23:06 PM    schema: undefined,
Aug 2 10:23:06 PM    table: undefined,
Aug 2 10:23:06 PM    column: undefined,
Aug 2 10:23:06 PM    dataType: undefined,
Aug 2 10:23:06 PM    constraint: undefined,
Aug 2 10:23:06 PM    file: 'miscinit.c',
Aug 2 10:23:06 PM    line: '734',
Aug 2 10:23:06 PM    routine: 'InitializeSessionUserId'
Aug 2 10:23:06 PM  }

```
