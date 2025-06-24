# Soundcraft Control - Stream Deck Plugin

Control your Soundcraft UI 16 mixer directly from your Elgato Stream Deck! Perfect for musicians, podcast creators, content streamers, and professionals managing multiple audio sources across different applications and meetings.

## 🎵 Who This Is For

### Musicians & Content Creators
- **Live Streaming**: Quick mute/unmute between songs or during breaks
- **Recording**: Instant volume adjustments without touching the mixer
- **Performance**: Trigger custom audio effects and routing changes
- **Podcast Production**: Seamless intro/outro music and guest audio control

### Professional Audio Management
- **Multi-Computer Setups**: Control shared audio interface from any workstation
- **Video Conferencing**: Manage different meeting audio levels simultaneously
- **Presentation Audio**: Quick audio routing for demos and presentations
- **Broadcasting**: Professional audio control for live shows and streams

### Business & Remote Work
- **Multiple Meetings**: Attend several meetings while controlling which audio goes where
- **Audio Switching**: Route different computers to headphones vs speakers
- **Quick Muting**: Instant mute for any channel during calls
- **Volume Management**: Precise control over meeting, system, and music levels

## ✨ Features

### Two Powerful Actions

#### 1. **Soundcraft Custom Action**
Execute any custom Soundcraft command with a single button press.

**Perfect for:**
- Routing audio between channels
- Triggering complex mixer configurations  
- Setting up custom EQ and effects
- Switching between different audio scenes

#### 2. **Soundcraft Volume Controller** 
Dedicated volume and mute control with visual feedback.

**Perfect for:**
- Quick volume adjustments during live situations
- Emergency muting during calls or streams
- Fine-tuned volume control with custom step sizes
- Stereo channel control for music playback

### Advanced Features

#### 🎧 **Stereo Channel Support**
Control stereo pairs effortlessly:
- **Mono channels**: `a.0` (single channel)
- **Stereo pairs**: `l.0,l.1` (both channels controlled together)
- **Multiple channels**: `a.0,a.1,a.2` (group control)

#### 🔄 **Real-Time Feedback**
- **Live volume display**: See exact volume percentages on your Stream Deck
- **Mute indicators**: [M] shows when channels are muted
- **Connection status**: Know when your mixer is connected or offline
- **Visual confirmation**: Button feedback shows command execution

#### ⚡ **Smart Controls**
- **Long-press mute**: Hold volume buttons to toggle mute (configurable)
- **Custom step sizes**: Precise volume control (1% to 10% increments)
- **Multi-channel commands**: Send complex commands to multiple channels at once
- **Error handling**: Clear error messages when connection issues occur

## 🚀 Quick Setup

### 1. **Network Setup**
- Connect your Soundcraft UI 16 to your network via Ethernet
- Find the mixer's IP address (usually shown on mixer display or router admin)
- Ensure your computer and mixer are on the same network

### 2. **Plugin Configuration**

#### For Custom Commands:
1. **IP Address**: Enter your mixer's IP (e.g., `192.168.1.100`)
2. **Channel Name**: Target channel (e.g., `a.0`, `i.1`, `l.0`)
3. **Commands**: Enter commands (one per line):
   ```
   3:::SETD^{channel}.mute^0
   3:::SETD^{channel}.gain^0.75
   ```
4. **Display Options**: Choose what to show on the button

#### For Volume Control:
1. **IP Address**: Enter your mixer's IP
2. **Channel Name**: 
   - Single channel: `a.0`
   - Stereo pair: `l.0,l.1`
3. **Volume Action**: Choose Increase or Decrease
4. **Step Size**: How much to change volume per press (default: 5%)
5. **Display Options**: Show mute state and/or volume percentage

### 3. **Common Channel Names**
- **Analog Inputs**: `a.0`, `a.1`, `a.2`, etc.
- **Digital Inputs**: `i.0`, `i.1`, `i.2`, etc.
- **Line Outputs**: `l.0`, `l.1` (often stereo pairs)
- **Auxiliary Sends**: `aux.0`, `aux.1`, etc.

## 💡 Usage Examples

### Example 1: Podcast Setup
**Goal**: Quick intro music control

**Custom Action Button**: "Intro Music"
- **Channel**: `l.0,l.1` (stereo music input)
- **Commands**: 
  ```
  3:::SETD^l.0.mute^0
  3:::SETD^l.1.mute^0
  3:::SETD^l.0.mix^0.8
  3:::SETD^l.1.mix^0.8
  ```

**Volume Control Button**: "Music Volume"
- **Channel**: `l.0,l.1`
- **Action**: Decrease Volume
- **Step Size**: 10%
- **Long Press Mute**: Enabled

### Example 2: Multi-Meeting Setup
**Goal**: Manage audio from two different meeting platforms

**Volume Buttons**:
- **Meeting 1**: Channel `a.0` (Computer 1 input)
- **Meeting 2**: Channel `a.1` (Computer 2 input)
- **Master Out**: Channel `l.0,l.1` (to speakers/headphones)

Each button can independently control volume and mute for different meetings.

### Example 3: Live Streaming
**Goal**: Professional audio switching during stream

**Custom Actions**:
- **"Music Only"**: Unmute music, mute microphone
- **"Talk Only"**: Unmute microphone, mute music  
- **"Both"**: Unmute everything
- **"Silent"**: Mute everything

### Example 4: Recording Studio
**Goal**: Quick monitor mix adjustments

**Volume Controllers**:
- **Instruments**: `a.0,a.1` (stereo instrument input)
- **Vocals**: `a.2` (vocal microphone)
- **Playback**: `l.0,l.1` (DAW playback)
- **Headphones**: `aux.0` (headphone send)

## 🔧 Advanced Tips

### Command Syntax
Commands use the format: `3:::SETD^[channel].[parameter]^[value]`

**Common Parameters**:
- `mix` - Main volume level (0.0 to 1.0)
- `mute` - Mute state (0 = unmuted, 1 = muted)
- `gain` - Input gain (0.0 to 1.0)
- `aux.0` - Auxiliary send level

### Stereo Channel Best Practices
- Always list the left channel first: `l.0,l.1` not `l.1,l.0`
- Status display comes from the first channel listed
- Both channels receive the same commands simultaneously

### Troubleshooting
- **"Connection Error"**: Check mixer IP address and network connection
- **"No Channel Data"**: Verify channel name matches mixer configuration
- **Commands not working**: Ensure proper command syntax and channel names

## 🎯 Use Cases by Profession

### **Content Creators**
- Stream intro/outro music control
- Guest audio management
- Background music ducking
- Emergency mute for phone calls

### **Musicians**
- Live performance backing tracks
- In-ear monitor mixing
- Recording session monitoring
- Quick instrument muting between songs

### **Business Professionals**
- Conference room audio routing
- Multiple meeting participation
- Presentation audio control
- Quick mute for confidential discussions

### **Broadcasters**
- On-air/off-air switching
- Commercial break automation
- Caller audio management
- Emergency broadcast controls

## 🛠️ Technical Requirements

- **Mixer**: Soundcraft UI 16 (other UI series may work)
- **Network**: Ethernet connection to mixer
- **Stream Deck**: Any Elgato Stream Deck model
- **Software**: Stream Deck Software 6.5 or later

## 📞 Support

Having issues? Check these common solutions:

1. **Can't connect to mixer**:
   - Verify IP address in mixer settings
   - Check network connectivity
   - Ensure mixer and computer are on same network

2. **Commands not working**:
   - Double-check channel names
   - Verify command syntax
   - Test with simple commands first (mute/unmute)

3. **Volume control not responding**:
   - Confirm channel name is correct
   - Check if stereo channels are configured properly
   - Verify step size setting

---

Transform your audio workflow with professional mixer control at your fingertips! 🎛️✨