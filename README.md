# react-leap [![Build Status](https://travis-ci.org/pawelgalazka/react-leap.svg?branch=master)](https://travis-ci.org/pawelgalazka/react-leap) [![npm version](https://badge.fury.io/js/react-leap.svg)](https://badge.fury.io/js/react-leap)
Leap Motion for ReactJS

## Quick start

Setup `LeapProvider`:

```jsx
import React from 'react';
import { LeapProvider } from 'react-leap'
import MyApp from './myapp'

const AppShell = () => (
  <div>
    <LeapProvider options={{enableGestures: true}}>
      <MyApp />
    </LeapProvider>
  </div>
)

export default AppShell
```

Connect Leap data to your app (`myapp.js`):

```jsx

import React from 'react'
import { withLeapContainer } from 'react-leap'

const MyApp = ({frame}) => {
  const hands = frame.hands
  
  // process data from frame

  return (
    <div>
    </div>
  )
}

export default withLeapContainer(MyApp)
```
