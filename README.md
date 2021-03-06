# circleci-typescript-axios
[![circleci-typescript-axios](https://circleci.com/gh/cob16/circleci-typescript-axios/tree/master.svg?style=svg)](https://circleci.com/gh/cob16/circleci-typescript-axios/tree/master)

Autogenerated sdk for circle ci v2

**Warning** the circle v2 api is in preview and is **currently making braking changes** see [breaking.md](https://github.com/CircleCI-Public/api-preview-docs/blob/master/docs/breaking.md)

[See the full doc here](https://cob16.github.io/circleci-typescript-axios/)

# Getting started
```bash
npm i circleci-typescript-axios --save
```
or to build form source 
```bash
git clone https://github.com/cob16/circleci-typescript-axios.git
cd circleci-typescript-axios
npm install
npm run build
```


Example Usage
```typescript
import { PreviewApiFactory, Project } from 'circleci-typescript-axios';

let client = PreviewApiFactory({
  apiKey: '<MY-API-KEY>',
});

client
  .getProjectBySlug('gh/cob16/circleci-lib')
  .then(resp => {
    let project: Project = resp.data;
    console.log(project.name);
    console.log(project.organization_name);
    console.log(project.slug);
    console.log(project.vcs_info);
  })
  .catch(error => {
    console.log(error);
  });
```
To see other methods [See the full doc here](https://cob16.github.io/circleci-typescript-axios/)

