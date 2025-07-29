# Soundcraft Control - Stream Deck Plugin

Control your Soundcraft UI 16 mixer directly from your Elgato Stream Deck! Perfect for musicians, podcast creators, content streamers, and professionals managing multiple audio sources across different applications and meetings.

## 🎵 Who This Is For

### Musicians & Content Creators
- **Live Streaming**: Quick mute/unmute between songs or during breaks
- **Recording**: Instant volume adjustments without touching the mixer
- **Performance**: Trigger custom audio effects and routing changes
- **Podcast Production**: Seamless intro/outro music and guest audio control

### Entertainment & Cinema & Events
- **Mobile Cinema Operations**: Professional sound control for outdoor movie screenings
- **Event Audio Management**: Live sound mixing for festivals, markets, and community events  
- **Venue Sound Systems**: Real-time audio control for restaurants, bars, and entertainment venues
- **Multi-Zone Audio**: Independent control of different audio areas (lobby, main area, concessions)
- **Background Music Control**: Seamless transitions between ambient music and live audio

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

### Eight Powerful Actions

#### 1. **Soundcraft Custom Action**
Execute any custom Soundcraft command with a single button press.

**Perfect for:**
- Routing audio between channels
- Triggering complex mixer configurations  
- Setting up custom EQ and effects
- Switching between different audio scenes

#### 2. **Soundcraft Button Volume Controller** 
Dedicated volume and mute control for Stream Deck buttons with visual feedback.

**Perfect for:**
- Quick volume adjustments with button presses
- Emergency muting with long-press functionality
- Fine-tuned volume control with custom step sizes
- Stereo channel control for music playback

#### 3. **Soundcraft Dial Volume Controller**
Professional volume and mute control for Stream Deck dials with real-time visual feedback.

**Perfect for:**
- Smooth volume adjustments by rotating the dial
- Instant mute toggle by pressing the dial
- Real-time visual feedback with percentage display and horizontal bar
- Professional mixing workflows with tactile control

#### 4. **Soundcraft Advanced Dial Controller** 🆕
Multi-parameter control system for professional audio engineering with Stream Deck dials.

**Perfect for:**
- Professional mixing with multiple parameter control per dial
- EQ adjustment workflows (frequency, Q factor, gain)
- De-esser fine-tuning (frequency, threshold, ratio)
- Gain staging and volume control in one device
- Custom-labeled controls for complex setups

#### 5. **Soundcraft Toggle Mute/Solo Action** 🆕
Dedicated mute and solo toggle control with real-time status indicators.

**Perfect for:**
- Quick mute/unmute control with [M] indicator
- Solo channel control with [S] indicator
- Combined mute/solo functionality on single button
- Real-time status updates from mixer
- Volume level display with toggle controls

#### 6. **Soundcraft Pan Toggle Action** 🆕
Professional pan position control with one-button cycling between Left, Center, and Right positions.

**Perfect for:**
- Quick pan adjustments with [L], [C], [R] indicators
- Professional stereo field management
- Real-time pan position feedback from mixer
- Combined pan control with mute/volume display
- Stereo channel pan synchronization

#### 7. **Soundcraft Custom Dial Action** 🆕
Universal parameter control system allowing you to control ANY mixer parameter using encoder dials.

**Perfect for:**
- Effects control (reverb, delay, chorus) with `fx.0.value^`, `fx.1.value^`, `fx.2.value^`
- Custom EQ adjustments with any EQ parameter
- Professional de-esser control with `deesser.threshold^`
- Advanced gain staging with `gain^` parameter
- Pan control with `pan^` parameter
- Any mixer parameter with real-time percentage display

#### 8. **Soundcraft Custom Parameter Button Control** 🆕
Universal parameter control system allowing you to control ANY mixer parameter using buttons with increase/decrease functionality.

**Perfect for:**
- Effects buttons (Reverb+, Reverb-, Delay+, Delay-) with `fx.0.value^`, `fx.1.value^`, `fx.2.value^`
- Pan control buttons (Pan Left, Pan Right) with `pan^` parameter
- Gain control buttons (Gain+, Gain-) with `gain^` parameter
- EQ adjustment buttons with any EQ parameter
- Precise parameter stepping with configurable step sizes
- Long-press mute functionality for emergency control

### Advanced Features

#### 🎧 **Stereo Channel Support**
Control stereo pairs effortlessly:
- **Mono channels**: `a.0` (single channel)
- **Stereo pairs**: `l.0,l.1` (both channels controlled together)
- **Multiple channels**: `a.0,a.1,a.2` (group control)

#### 🔄 **Real-Time Feedback**
- **Live volume display**: See exact volume percentages on your Stream Deck
- **Mute indicators**: [M] shows when channels are muted
- **Solo indicators**: [S] shows when channels are solo
- **Pan indicators**: [L], [C], [R] show current pan position
- **Connection status**: Know when your mixer is connected or offline
- **Visual confirmation**: Button feedback shows command execution

#### ⚡ **Smart Controls**
- **Button Controls**: Short press for volume, long-press for mute (configurable)
- **Dial Controls**: Rotate for volume, press for mute (configurable)
- **Advanced Dial Controls**: Rotate to adjust current parameter, press to cycle parameters
- **Parameter Cycling**: Switch between Volume, Gain, EQ, and De-esser settings
- **Visual Feedback**: Real-time horizontal bar and percentage display on dials
- **Custom Labeling**: Button titles prefix parameter names (e.g., "J1 Volume", "Master EQ Gain")
- **Custom step sizes**: Precise control (1% to 10% increments)
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

#### For Button Volume Control:
1. **IP Address**: Enter your mixer's IP
2. **Channel Name**: 
   - Single channel: `a.0`
   - Stereo pair: `l.0,l.1`
3. **Volume Action**: Choose Increase or Decrease
4. **Step Size**: How much to change volume per press (default: 5%)
5. **Long Press Mute**: Enable mute toggle on button hold
6. **Display Options**: Show mute state and/or volume percentage

#### For Dial Volume Control:
1. **IP Address**: Enter your mixer's IP
2. **Channel Name**: 
   - Single channel: `a.0`
   - Stereo pair: `l.0,l.1`
3. **Step Size**: How much to change volume per rotation tick (default: 5%)
4. **Dial Press Mute**: Enable mute toggle when pressing the dial
5. **Display Options**: Show mute state and/or volume percentage
   - Visual horizontal bar shows volume level in real-time
   - Percentage and mute status appear in dial's {{value}} area

#### For Advanced Dial Control: 🆕
1. **IP Address**: Enter your mixer's IP
2. **Channel Name**: 
   - Single channel: `i.2` (input channels work best)
   - Stereo pair: `i.2,i.3`
3. **Step Size**: How much to change parameters per rotation tick (default: 5%)
4. **Button Title**: Custom label (e.g., "J1", "Master", "Vocal") - appears before parameter name
5. **Active Parameters**: Select which parameters to control:
   - ☐ Volume (mix level)
   - ☐ Gain (input gain)
   - ☐ EQ Frequency (EQ band 1 frequency)
   - ☐ EQ Q Factor (EQ band 1 Q factor)
   - ☐ EQ Gain (EQ band 1 gain)
   - ☐ De-Esser Frequency
   - ☐ De-Esser Threshold  
   - ☐ De-Esser Ratio
6. **Display Options**: Show parameter percentage values
   - Visual horizontal bar shows current parameter level
   - Parameter name and custom label shown in title

#### For Toggle Mute/Solo Action: 🆕
1. **IP Address**: Enter your mixer's IP
2. **Channel Name**: 
   - Single channel: `a.0`
   - Stereo pair: `l.0,l.1`
3. **Toggle Options**: Select which controls to enable:
   - ☐ Toggle Mute - Shows [M] when muted
   - ☐ Toggle Solo - Shows [S] when solo
4. **Display Options**:
   - ☐ Show Volume Level - Display volume percentage
   - Button Title: Custom label (optional)
5. **Button Press**: Toggles selected mute/solo states

#### For Pan Toggle Action: 🆝
1. **IP Address**: Enter your mixer's IP
2. **Channel Name**: 
   - Single channel: `i.2`
   - Stereo pair: `i.2,i.3`
3. **Button Title**: Custom label (optional)
4. **Display Options**:
   - ☐ Show Mute State - Display [M] when muted
   - ☐ Show Volume Level - Display volume percentage
5. **Button Press**: Cycles pan through Left (0.0) → Center (0.5) → Right (1.0)
6. **Pan Display**: Shows [L], [C], [R], or N/A for other positions

#### For Custom Dial Action: 🆕
1. **IP Address**: Enter your mixer's IP
2. **Channel Name**: 
   - Single channel: `i.2`
   - Stereo pair: `i.2,i.3`
3. **Custom Dial Parameter**: Enter any mixer parameter:
   - **Effects**: `fx.0.value^` (reverb), `fx.1.value^` (delay), `fx.2.value^` (chorus)
   - **Pan**: `pan^`
   - **Gain**: `gain^`
   - **EQ**: `eq.b1.freq^`, `eq.b1.gain^`
   - **De-esser**: `deesser.threshold^`
4. **Step Size**: Adjustment per dial rotation (default: 0.05)
5. **Optional Settings**:
   - ☐ Mute on Dial Press - Toggle mute when pressing dial
   - ☐ Show Mute State - Display [M] when muted
   - Button Title: Custom label (e.g., "Vocal Reverb")
6. **Dial Display**: Shows parameter percentage (0-100%) with visual bar

#### For Custom Parameter Button Control: 🆕
1. **IP Address**: Enter your mixer's IP
2. **Channel Name**: 
   - Single channel: `i.2`
   - Stereo pair: `i.2,i.3`
3. **Custom Parameter**: Enter any mixer parameter:
   - **Effects**: `fx.0.value^` (reverb), `fx.1.value^` (delay), `fx.2.value^` (chorus)
   - **Pan**: `pan^`
   - **Gain**: `gain^`
   - **EQ**: `eq.b1.freq^`, `eq.b1.gain^`
   - **De-esser**: `deesser.threshold^`
4. **Increase Parameter Value**: 
   - ☑ **Checked**: Button press increases parameter value (e.g., "Reverb+")
   - ☐ **Unchecked**: Button press decreases parameter value (e.g., "Reverb-")
5. **Step Size**: Adjustment per button press (default: 0.05)
6. **Optional Settings**:
   - ☐ Toggle Mute on Long Press - Hold button to mute
   - ☐ Show Mute State - Display [M] when muted
   - Button Title: Custom label (e.g., "Vocal Reverb+")
7. **Button Display**: Shows parameter percentage (0-100%) in title

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

**Button Volume Control**: "Music Volume"
- **Channel**: `l.0,l.1`
- **Action**: Decrease Volume
- **Step Size**: 10%
- **Long Press Mute**: Enabled

**Dial Volume Control**: "Music Level"
- **Channel**: `l.0,l.1`
- **Step Size**: 5%
- **Dial Press Mute**: Enabled
- **Visual Display**: Shows percentage and horizontal bar in real-time

**Advanced Dial Control**: "Music Master"
- **Channel**: `l.0,l.1`
- **Button Title**: "Music"
- **Active Parameters**: Volume, EQ Frequency, EQ Gain
- **Usage**: Press dial to cycle between "Music Volume", "Music EQ Frequency", "Music EQ Gain"

**Toggle Mute/Solo Action**: "Quick Mute"
- **Channel**: `l.0,l.1`
- **Toggle Options**: Mute enabled, Solo disabled
- **Button Title**: "Music"
- **Usage**: Press to toggle mute, shows "[M] Music" when muted

**Pan Toggle Action**: "Music Pan"
- **Channel**: `l.0,l.1`
- **Button Title**: "Music"
- **Display Options**: Show Volume Level enabled
- **Usage**: Press to cycle pan: Left → Center → Right → Left, shows "[L] Music 80%" or "[C] Music 80%"

### Example 2: Multi-Meeting Setup
**Goal**: Manage audio from two different meeting platforms

**Volume Controls**:
- **Meeting 1 (Button)**: Channel `a.0` (Computer 1 input)
- **Meeting 2 (Button)**: Channel `a.1` (Computer 2 input)  
- **Master Out (Advanced Dial)**: Channel `l.0,l.1` (to speakers/headphones)
  - **Button Title**: "Master"
  - **Active Parameters**: Volume, EQ Frequency, EQ Gain
  - **Usage**: Cycle between "Master Volume", "Master EQ Frequency", "Master EQ Gain"

**Toggle Controls**:
- **Meeting 1 Mute (Toggle)**: Channel `a.0` - Quick mute toggle with [M] indicator
- **Meeting 2 Mute (Toggle)**: Channel `a.1` - Quick mute toggle with [M] indicator
- **Master Solo (Toggle)**: Channel `l.0,l.1` - Solo control with [S] indicator

**Pan Controls**:
- **Meeting 1 Pan (Pan Toggle)**: Channel `a.0` - Position meeting audio in stereo field
- **Meeting 2 Pan (Pan Toggle)**: Channel `a.1` - Independent pan control for second meeting
- **Master Pan (Pan Toggle)**: Channel `l.0,l.1` - Overall stereo positioning

Each control can independently manage volume, mute, solo, and pan for different audio sources.

### Example 3: Live Streaming
**Goal**: Professional audio switching during stream

**Custom Actions**:
- **"Music Only"**: Unmute music, mute microphone
- **"Talk Only"**: Unmute microphone, mute music  
- **"Both"**: Unmute everything
- **"Silent"**: Mute everything

### Example 4: Recording Studio
**Goal**: Quick monitor mix adjustments

**Professional Setup**:
- **Instruments (Advanced Dial)**: `i.0,i.1` 
  - **Title**: "Inst", **Parameters**: Volume, Gain, EQ Frequency, EQ Q, EQ Gain
- **Vocals (Advanced Dial)**: `i.2`
  - **Title**: "Vocal", **Parameters**: Volume, Gain, De-Esser Freq, De-Esser Threshold, De-Esser Ratio
- **Playback (Dial)**: `l.0,l.1` (DAW playback with smooth control)
- **Monitor (Button)**: `aux.0` (headphone send with long-press mute)

### Example 5: Advanced Dial Workflow 🆕
**Goal**: Professional vocal processing with single dial

**Setup**: Advanced Dial Controller
- **Channel**: `i.2` (vocal microphone input)
- **Button Title**: "J1"
- **Active Parameters**: Volume, Gain, De-Esser Frequency, De-Esser Threshold

**Workflow**:
1. **"J1 Volume"** - Set overall vocal level in mix
2. **Press dial** → **"J1 Gain"** - Adjust input gain for optimal signal
3. **Press dial** → **"J1 De-Esser Frequency"** - Target sibilant frequencies
4. **Press dial** → **"J1 De-Esser Threshold"** - Set de-esser sensitivity
5. **Press dial** → Returns to **"J1 Volume"**

**Result**: Complete vocal chain control with one dial, real-time visual feedback, and clear parameter identification.

### Example 6: Professional Effects Control 🆕
**Goal**: Complete effects processing for vocals using Custom Dial Actions

**Setup**: Four Custom Dial Actions controlling vocal channel i.2

**Vocal Reverb Control**:
- **Channel**: `i.2`
- **Custom Dial Parameter**: `fx.0.value^`
- **Button Title**: "Vocal Reverb"
- **Usage**: Rotate to add room ambience (0% = dry, 100% = wet)

**Vocal Delay Control**:
- **Channel**: `i.2` 
- **Custom Dial Parameter**: `fx.1.value^`
- **Button Title**: "Vocal Delay"
- **Usage**: Rotate to add echo effect (0% = no delay, 100% = full delay)

**Vocal Chorus Control**:
- **Channel**: `i.2`
- **Custom Dial Parameter**: `fx.2.value^`
- **Button Title**: "Vocal Chorus"
- **Usage**: Rotate to add width and texture (0% = no chorus, 100% = full chorus)

**Vocal De-esser Control**:
- **Channel**: `i.2`
- **Custom Dial Parameter**: `deesser.threshold^`
- **Button Title**: "Vocal DeEss"
- **Usage**: Rotate to control sibilance (0% = no processing, 100% = maximum reduction)

**Professional Workflow**:
1. **Set base vocal level** with volume control
2. **Add spatial depth** with Vocal Reverb dial (typically 15-30%)
3. **Create rhythmic interest** with Vocal Delay dial (typically 10-25%)
4. **Enhance vocal width** with Vocal Chorus dial (typically 5-15%)
5. **Control harsh "S" sounds** with Vocal DeEss dial (adjust until sibilance is controlled)
6. **Emergency mute** by pressing any dial

**Result**: Complete professional vocal processing with real-time visual feedback showing exact effect percentages.

### Example 7: Professional Button Effects Control 🆕
**Goal**: Precise effects adjustment using Custom Parameter Button Controls

**Setup**: Six Custom Parameter Button Controls for vocal channel i.2

**Reverb Control Buttons**:
- **Reverb+ Button**:
  - **Channel**: `i.2`
  - **Custom Parameter**: `fx.0.value^`
  - **Increase Parameter Value**: ☑ Checked
  - **Button Title**: "Vocal Reverb+"
  - **Usage**: Each press adds 5% reverb

- **Reverb- Button**:
  - **Channel**: `i.2`
  - **Custom Parameter**: `fx.0.value^`
  - **Increase Parameter Value**: ☐ Unchecked
  - **Button Title**: "Vocal Reverb-"
  - **Usage**: Each press removes 5% reverb

**Delay Control Buttons**:
- **Delay+ Button**:
  - **Channel**: `i.2`
  - **Custom Parameter**: `fx.1.value^`
  - **Increase Parameter Value**: ☑ Checked
  - **Button Title**: "Vocal Delay+"

- **Delay- Button**:
  - **Channel**: `i.2`
  - **Custom Parameter**: `fx.1.value^`
  - **Increase Parameter Value**: ☐ Unchecked
  - **Button Title**: "Vocal Delay-"

**Pan Control Buttons**:
- **Pan Left Button**:
  - **Channel**: `i.2`
  - **Custom Parameter**: `pan^`
  - **Increase Parameter Value**: ☐ Unchecked
  - **Button Title**: "Pan Left"
  - **Usage**: Moves pan toward left (0%)

- **Pan Right Button**:
  - **Channel**: `i.2`
  - **Custom Parameter**: `pan^`
  - **Increase Parameter Value**: ☑ Checked
  - **Button Title**: "Pan Right"
  - **Usage**: Moves pan toward right (100%)

**Professional Button Workflow**:
1. **Start with dry vocal** - All effects at 0%
2. **Add reverb gradually** - Press "Vocal Reverb+" 3-6 times (15-30%)
3. **Add delay sparingly** - Press "Vocal Delay+" 2-5 times (10-25%)
4. **Position in stereo field** - Use "Pan Left"/"Pan Right" as needed
5. **Fine-tune effects** - Use + and - buttons for precise control
6. **Emergency mute** - Long press any button (if enabled)

**Real-Time Feedback**: Both "Reverb+" and "Reverb-" buttons show the same current percentage (e.g., "Vocal Reverb+ | 25%" and "Vocal Reverb- | 25%"), updating instantly when either is pressed.

**Result**: Precise, tactile control over effects with immediate visual feedback and synchronized button displays.

## 🔧 Advanced Tips

### Advanced Dial Controller Pro Tips 🆕

#### **Parameter Selection Strategy**
- **Volume + Gain**: Perfect for input level management
- **EQ Trilogy**: Use Frequency + Q Factor + Gain for complete EQ control
- **De-esser Suite**: Frequency + Threshold + Ratio for vocal processing
- **Custom Combos**: Mix and match based on your workflow needs

#### **Efficient Workflows**
- **Label Everything**: Use descriptive button titles ("J1", "Vocal", "Master")
- **Group by Function**: Create separate dials for different processing stages
- **Start Simple**: Begin with Volume + Gain, add EQ parameters as needed
- **Channel Strategy**: Input channels (`i.x`) work best for gain/EQ/de-esser

#### **Visual Feedback Mastery**
- **Real-time Values**: Enable "Show Level (%)" to see exact parameter values
- **Parameter Identification**: Button title + parameter name shows clearly (e.g., "J1 EQ Gain")
- **Quick Reference**: Current parameter always visible in dial title
- **Progress Indication**: Horizontal bar gives instant visual feedback

### Custom Dial Action Pro Tips 🆕

#### **Effects Control Strategy**
- **Reverb** (`fx.0.value^`): Start subtle (15-30%), add gradually for space
- **Delay** (`fx.1.value^`): Use sparingly (10-25%) to avoid muddiness
- **Chorus** (`fx.2.value^`): Less is more (5-15%) for natural width enhancement
- **Layer Effects**: Combine multiple effects for rich, professional sound

#### **Parameter Discovery**
- **Standard Parameters**: `pan^`, `gain^`, `mute^`, `solo^`
- **EQ Parameters**: `eq.b1.freq^`, `eq.b1.q^`, `eq.b1.gain^` (for EQ band 1)
- **Dynamics**: `deesser.threshold^`, `deesser.ratio^`, `deesser.freq^`
- **Effects**: `fx.0.value^`, `fx.1.value^`, `fx.2.value^` (FX sends)
- **Experiment**: Try other parameter names - the system supports ANY parameter!

#### **Efficient Workflows**
- **Name Everything**: Use descriptive titles like "Vocal Reverb" not just "Reverb"
- **Group by Function**: Place related controls together (all vocal effects)
- **Visual Feedback**: Watch percentage displays for precise control
- **Mute Integration**: Enable "Mute on Dial Press" for emergency controls

#### **Professional Setup Examples**
- **Vocal Chain**: Gain → De-esser → Reverb → Delay
- **Instrument Effects**: EQ Freq → EQ Gain → Chorus → Reverb  
- **Master Bus**: Pan → Volume (using standard controllers) + Effects (Custom Dial)

### Command Syntax
Commands use the format: `3:::SETD^[channel].[parameter]^[value]`

**Basic Parameters**:
- `mix` - Main volume level (0.0 to 1.0)
- `mute` - Mute state (0 = unmuted, 1 = muted)
- `gain` - Input gain (0.0 to 1.0)
- `aux.0` - Auxiliary send level

**Advanced Parameters** (Advanced Dial Controller & Pan Toggle Action):
- `pan` - Pan position (0.0 = Left, 0.5 = Center, 1.0 = Right)
- `solo` - Solo state (0 = not solo, 1 = solo)
- `eq.b1.freq` - EQ band 1 frequency (0.0 to 1.0)
- `eq.b1.q` - EQ band 1 Q factor (0.0 to 1.0)
- `eq.b1.gain` - EQ band 1 gain (0.0 to 1.0)
- `deesser.freq` - De-esser frequency (0.0 to 1.0)
- `deesser.threshold` - De-esser threshold (0.0 to 1.0)
- `deesser.ratio` - De-esser ratio (0.0 to 1.0)

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
- Stream intro/outro music control with Advanced Dial (Volume + EQ)
- Guest audio management with multi-parameter control
- Background music ducking and EQ adjustment
- Emergency mute for phone calls with Toggle Mute/Solo Action
- Quick solo isolation for specific audio sources
- Professional stereo positioning with Pan Toggle Action

### **Musicians**
- Live performance backing tracks with real-time EQ
- In-ear monitor mixing with Advanced Dial Controllers
- Recording session monitoring with gain staging control
- Quick instrument processing (Volume + Gain + De-esser)
- Instant mute/solo for individual instruments during practice
- Professional stereo field control with Pan Toggle Action

### **Business Professionals**
- Conference room audio routing
- Multiple meeting participation with individual EQ control
- Presentation audio control with Advanced Dial flexibility
- Quick mute for confidential discussions with Toggle Actions
- Solo specific meeting audio when needed

### **Broadcasters**
- On-air/off-air switching with full audio processing
- Commercial break automation
- Caller audio management with real-time de-esser control
- Emergency broadcast controls with Advanced Dial backup
- Instant mute/solo for live show management

### **Audio Engineers** 🆕
- Multi-parameter control for complex mixes
- Real-time EQ adjustment during live performances
- De-esser fine-tuning for vocal processing
- Gain staging and level management with visual feedback

### **Entertainment & Venue Operators** 🆕
- Mobile cinema sound control for outdoor screenings
- Event audio management for festivals and markets
- Multi-zone venue control (lobby, dining, main area)
- Background music transitions during live events
- Quick audio adjustments for different entertainment segments

## 🛠️ Technical Requirements

- **Mixer**: Soundcraft UI 16 (other UI series may work)
- **Network**: Ethernet connection to mixer
- **Stream Deck**: Any Elgato Stream Deck model
- **Software**: Stream Deck Software 6.5 or later

## 📞 Support & Professional Services

### Technical Support
Having issues? Check these common solutions first:

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

4. **Toggle actions not working**:
   - Ensure at least one toggle option (mute or solo) is selected
   - Verify channel supports mute/solo operations
   - Check mixer connection status

5. **Pan toggle not responding**:
   - Confirm channel supports pan control
   - Verify pan values are updating on mixer
   - Check that N/A displays for non-standard pan positions

For direct technical support, contact us at **support@doitwise.co**

### Professional Services

#### 🎯 **Free 30-Minute Consultation**
Get personalized guidance on optimizing your plugin setup and audio workflow. Our experts will help you:
- Configure actions for your specific use case
- Design efficient control layouts for your Stream Deck
- Optimize mixer settings for your application
- Troubleshoot complex setup scenarios

#### 🎛️ **Audio Workflow Programming**
Professional Soundcraft UI mixer programming services:
- Custom audio routing configurations
- Complex multi-zone setups
- Performance-optimized mixer scenes
- Integration with broadcast and streaming systems
- Professional venue audio system design

#### 🚀 **Plugin Feature Extensions**
Need additional functionality? We offer custom plugin development:
- New action types for specialized workflows
- Integration with other audio software
- Custom visual feedback and indicators
- Advanced automation features
- Enterprise-specific requirements

#### 💼 **Custom Development Solutions**
Complete audio control system development:
- Bespoke Stream Deck plugins for any audio hardware
- Integration with professional audio software (Pro Tools, Logic, etc.)
- Custom hardware integration solutions
- Workflow automation systems
- Multi-platform audio control applications

**Ready to enhance your audio workflow?** Contact us at **support@doitwise.co** to discuss your requirements and receive a personalized consultation.

---

Transform your audio workflow with professional mixer control at your fingertips! 🎛️✨
