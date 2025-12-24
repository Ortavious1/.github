itslittv-app
├── App.js
├── app.json
├── package.json
├── assets/
│   └── icon.png


{
  "expo": {
    "name": "ItsLitTV",
    "slug": "itslittv",
    "version": "1.0.0",
    "orientation": "portrait",
    "icon": "./assets/icon.png",
    "userInterfaceStyle": "dark",
    "splash": {
      "resizeMode": "contain",
      "backgroundColor": "#000000"
    },
    "assetBundlePatterns": ["**/*"]
  }
}


{
  "name": "itslittv",
  "version": "1.0.0",
  "main": "node_modules/expo/AppEntry.js",
  "scripts": {
    "start": "expo start"
  },
  "dependencies": {
    "expo": "~51.0.0",
    "react": "18.2.0",
    "react-native": "0.74.0"
  }
}

import React from 'react';
import { View, Text, StyleSheet, ScrollView, TouchableOpacity } from 'react-native';

export default function App() {
  return (
    <View style={styles.container}>
      <Text style={styles.title}>ITS LIT TV</Text>

      <ScrollView>
        <Episode title="Episode 1" />
        <Episode title="Episode 2" />
        <Episode title="Episode 3" />
        <Episode title="Episode 4" />
      </ScrollView>
    </View>
  );
}

function Episode({ title }) {
  return (
    <TouchableOpacity style={styles.card}>
      <Text style={styles.episodeTitle}>{title}</Text>
      <Text style={styles.subtitle}>Tap to watch</Text>
    </TouchableOpacity>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#000',
    paddingTop: 60,
    paddingHorizontal: 20
  },
  title: {
    color: '#ff4500',
    fontSize: 32,
    fontWeight: 'bold',
    marginBottom: 20,
    textAlign: 'center'
  },
  card: {
    backgroundColor: '#111',
    padding: 20,
    borderRadius: 12,
    marginBottom: 15
  },
  episodeTitle: {
    color: '#fff',
    fontSize: 20,
    fontWeight: '600'
  },
  subtitle: {
    color: '#888',
    marginTop: 5
  }
});Initial ItsLitTV streaming app
