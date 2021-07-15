# React Native - Tob Tab Navigation
Tob Tab Navigation Study :)

## Demo

<img src="https://user-images.githubusercontent.com/63582123/125743607-e44139b4-17dc-4b8e-a179-3888fdcd35f8.jpeg" width="347" height="599">
<img src="https://user-images.githubusercontent.com/63582123/125743597-e24023e2-6cd9-433d-a203-62d7a2ef30ba.jpeg" width="347" height="599">
<img src="https://user-images.githubusercontent.com/63582123/125743610-3ed38d8c-9b17-4e67-9edf-3d72682fd765.jpeg" width="347" height="599">

## Installation

```bash
npm install @react-navigation/material-top-tabs react-native-tab-view@^2.16.0
```

## Usage

### App.js

```jsx
import * as React from 'react';
import { Text, View } from 'react-native';
import { NavigationContainer } from '@react-navigation/native';
import { createMaterialTopTabNavigator } from '@react-navigation/material-top-tabs';

function HomeScreen() {
  return (
    <View style={{ flex: 1, justifyContent: 'center', alignItems: 'center', backgroundColor: '#fff1ff' }}>
      <Text style={{ fontSize: 30 }}>Home Screen</Text>
    </View>
  );
}

function ProfileScreen() {
  return (
    <View style={{ flex: 1, justifyContent: 'center', alignItems: 'center', backgroundColor: '#fff1ff' }}>
      <Text style={{ fontSize: 30 }}>Profile Screen</Text>
    </View>
  );
}

function SettingScreen() {
  return (
    <View style={{ flex: 1, justifyContent: 'center', alignItems: 'center', backgroundColor: '#fff1ff' }}>
      <Text style={{ fontSize: 30 }}>Setting Screen</Text>
    </View>
  );
}

const Tab = createMaterialTopTabNavigator();

export default function App() {
  return (
    <NavigationContainer>
      <Tab.Navigator tabBarOptions={{ 
        labelStyle: { fontSize: 12 }, 
        tabStyle: { height : 50 }, 
        style: { backgroundColor: '#e6ceff', marginTop: 20 },
        }}
      >
        <Tab.Screen name="Home" component={HomeScreen} />
        <Tab.Screen name="Profile" component={ProfileScreen} />
        <Tab.Screen name="Setting" component={SettingScreen} />
      </Tab.Navigator>
    </NavigationContainer>
  );
}
```