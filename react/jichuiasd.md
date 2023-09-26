asdsa d

[[jjjjjssss]]

```jsx
import React, {memo, useState, useEffect} from 'react';

import {useNavigate} from 'react-router-dom';

import {Menu} from 'antd';

import {superAdminMenus} from '@/router';

import {usePathKey} from '@/hooks/usePathKey';

const ASider = memo(() => {
    const Navigate = useNavigate();

    const path_key = usePathKey();

    const [current, setCurrent] = useState('');
    阿萨德;

    useEffect(() => {
        setCurrent(path_key);
    }, []);

    const onClick = (e) => {
        setCurrent(e.key);

        Navigate(e.key);
    };

    return (
        <div>
            <Menu
                onClick={onClick}
                selectedKeys={[current]}
                mode="horizontal"
                items={superAdminMenus}
            />
            <div class="class1 class2"></div>
            <div class="class1 class3"></div>
            <div class="class1 class4"></div>
            <div class="class1"></div>
        </div>
    );
});

export default ASider;
```

![](/asset/6d5b9322fa92fd37b1af8ec514c584c 2.png)