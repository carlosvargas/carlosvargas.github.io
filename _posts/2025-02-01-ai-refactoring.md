---
date: 2025-02-01 21:00:00 +0800
title: "Refactoring"
linkblog: true
tags: [llms]
---
I've been upgrading [Classmap's](https://classmap.org) React dependencies lately. [AntDesign](https://ant.design/) being one of these. During the v4 to v5 upgrade, they updated some components (Menu, Tabs) to move away from using React Children, and instead use an `items` property. 

I was dreading having to update all of the components impacted, until I realized that I could use Copilot (using GPT 4o) to do this for me. I was able to do these changes in about 10 minutes, instead of the hour or so it would have taken me to do manually.

Here's the propt I used:

```
Refactor these lines, so that instead of using React children, it uses an "items" property.

Here is an example:
\```
const items: MenuItem[] = [
  {
    label: 'Navigation One',
    key: 'mail',
    icon: <MailOutlined />,
  },
  {
    label: 'Navigation Three - Submenu',
    key: 'SubMenu',
    icon: <SettingOutlined />,
    children: [
      {
        type: 'group',
        label: 'Item 1',
        children: [
          { label: 'Option 1', key: 'setting:1' },
          { label: 'Option 2', key: 'setting:2' },
        ],
      }
    ],
  }]

 const [current, setCurrent] = useState('mail');

  const onClick: MenuProps['onClick'] = (e) => {
    console.log('click ', e);
    setCurrent(e.key);
  };


  <Menu onClick={onClick} mode="horizontal" items={items} />;
\```

the Menu.onClick has the following interface `function({ item, key, keyPath, domEvent })`
```