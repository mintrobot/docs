# Setup

Setup for the cylindrical robot arm is intentionally simple. The process is complete once the robot is powered, connected to the network, and accessible from a web browser.

## Package Contents

<div style="display:grid; grid-template-columns:repeat(4, minmax(0, 1fr)); gap:16px; align-items:start; margin:1.5rem 0;">
  <div style="border:1px solid rgba(255,255,255,0.08); border-radius:14px; padding:16px; background:rgba(255,255,255,0.02); text-align:center;">
    <img src="../images/robot-body-white.png" alt="Robot body" style="width:100%; max-width:150px; height:150px; object-fit:contain; margin:0 auto 12px auto; display:block;">
    <div style="font-weight:600;">Robot body</div>
  </div>
  <div style="border:1px solid rgba(255,255,255,0.08); border-radius:14px; padding:16px; background:rgba(255,255,255,0.02); text-align:center;">
    <img src="../images/adapter-white.png" alt="Dedicated adapter" style="width:100%; max-width:150px; height:150px; object-fit:contain; margin:0 auto 12px auto; display:block;">
    <div style="font-weight:600;">Dedicated adapter</div>
  </div>
  <div style="border:1px solid rgba(255,255,255,0.08); border-radius:14px; padding:16px; background:rgba(255,255,255,0.02); text-align:center;">
    <img src="../images/connection-cable-white.png" alt="Adapter-to-robot connection cable" style="width:100%; max-width:150px; height:150px; object-fit:contain; margin:0 auto 12px auto; display:block;">
    <div style="font-weight:600;">Connection cable</div>
  </div>
  <div style="border:1px solid rgba(255,255,255,0.08); border-radius:14px; padding:16px; background:rgba(255,255,255,0.02); text-align:center;">
    <img src="../images/power-cable-white.png" alt="Power cable" style="width:100%; max-width:150px; height:150px; object-fit:contain; margin:0 auto 12px auto; display:block;">
    <div style="font-weight:600;">Power cable</div>
  </div>
</div>

The package consists of:

- robot body x 1
- dedicated adapter x 1
- adapter-to-robot connection cable x 1
- power cable x 1

## Power Connection

Connect the dedicated adapter to the robot body using the supplied connection cable, then supply AC power to the adapter using the power cable.

<div style="display:grid; grid-template-columns:repeat(3, minmax(0, 1fr)); gap:16px; align-items:start; margin:1.5rem 0;">
  <div style="border:1px solid rgba(255,255,255,0.08); border-radius:14px; padding:16px; background:rgba(255,255,255,0.02); text-align:center;">
    <img src="../images/robot-connection-port-white.png" alt="Robot-side connection port" style="width:100%; max-width:180px; height:180px; object-fit:contain; margin:0 auto 12px auto; display:block;">
    <div style="font-weight:600;">Robot-side port</div>
  </div>
  <div style="border:1px solid rgba(255,255,255,0.08); border-radius:14px; padding:16px; background:rgba(255,255,255,0.02); text-align:center;">
    <img src="../images/adapter-connection-port-white.png" alt="Adapter-side connection port" style="width:100%; max-width:180px; height:180px; object-fit:contain; margin:0 auto 12px auto; display:block;">
    <div style="font-weight:600;">Adapter-side port</div>
  </div>
  <div style="border:1px solid rgba(255,255,255,0.08); border-radius:14px; padding:16px; background:rgba(255,255,255,0.02); text-align:center;">
    <img src="../images/adapter-power-port-white.png" alt="Adapter power input and power button" style="width:100%; max-width:180px; height:180px; object-fit:contain; margin:0 auto 12px auto; display:block;">
    <div style="font-weight:600;">Adapter power input</div>
  </div>
</div>

The three connection points shown above are:

- `Robot-side port`: connection cable input on the robot body
- `Adapter-side port`: connection cable input on the dedicated adapter
- `Adapter power input`: power cable input and power button on the adapter

The physical power path is:

1. connect the dedicated adapter to the robot body with the supplied connection cable
2. confirm the connection cable is fully seated on both the robot side and the adapter side
3. connect the power cable to the adapter power input
4. turn on the adapter with the power button if required
5. supply power to the adapter
6. confirm that the robot powers on together with the adapter

After the cable is connected, supply power to the adapter. Once the adapter is powered, the robot also powers on.

This completes the physical power setup.

## Network Connection

Because the robot uses an SDR-based control environment, communication is performed over LAN.

Connect an Ethernet cable to the LAN connector on the rear side of the robot, and connect the other end to the PC.

<figure markdown="span">
  ![Robot ethernet connection port](images/robot-ethernet-port-white.png){ width="360" }
  <figcaption>Ethernet connection port on the rear side of the robot</figcaption>
</figure>

<div class="setup-network-diagram">
  <div class="mermaid">
flowchart LR
    R["Cylindrical Robot Arm<br/>Default IP: 10.0.0.2"]
    C["RJ45 LAN Cable"]
    P["PC / Laptop<br/>Same Subnet Required"]
    R --- C --- P
  </div>
</div>

<style>
.setup-network-diagram {
  display: flex;
  justify-content: center;
  margin: 1.5rem 0;
}

.setup-network-diagram .mermaid {
  width: min(980px, 100%);
  margin: 0 auto;
}

.setup-network-diagram .mermaid svg {
  width: 100% !important;
  height: auto !important;
  display: block;
  margin: 0 auto;
}
</style>

## IP Configuration

The default IP address of the robot is `10.0.0.2`.

To communicate with the robot, the connected PC must use an IP address in the same subnet.

For example, the PC can be configured with an address such as `10.0.0.10`.

## Browser Access

Once the network is configured, open a web browser and enter the robot address.

If the connection is correct, the robot controller screen becomes available in the browser.

The controller software installed on the robot is Sodero Motion Studio.

Detailed Motion Studio usage should be referenced through `stellar-docs`.

<div style="display:grid; grid-template-columns:1fr 88px 1fr; gap:24px; align-items:start; margin:1.5rem 0;">
  <div style="border:1px solid rgba(255,255,255,0.08); border-radius:18px; background:rgba(255,255,255,0.02); padding:18px; display:flex; flex-direction:column;">
    <div style="text-align:center; font-weight:700; margin-bottom:14px;">Open Any Browser</div>
    <div style="flex:1; min-height:250px; display:flex; align-items:center; justify-content:center;">
      <div style="width:100%; max-width:400px; border:2px solid #3A475A; border-radius:18px; background:#232E3C;">
        <div style="height:34px; border-bottom:1px solid #3A475A; display:flex; align-items:center; padding:0 14px; gap:8px;">
          <span style="width:10px; height:10px; border-radius:50%; background:#FF5F57; display:inline-block;"></span>
          <span style="width:10px; height:10px; border-radius:50%; background:#FEBC2E; display:inline-block;"></span>
          <span style="width:10px; height:10px; border-radius:50%; background:#28C840; display:inline-block;"></span>
          <div style="margin-left:8px; flex:1; height:18px; border-radius:10px; background:#111823; border:1px solid #445064; color:#E1E7EF; font-size:0.74rem; display:flex; align-items:center; padding:0 10px;">http://10.0.0.2</div>
        </div>
        <div style="padding:22px 20px;">
          <div style="border:1px solid #445064; border-radius:12px; min-height:170px; background:#151C26; display:flex; flex-direction:column; align-items:center; justify-content:center;">
            <div style="font-size:1.45rem; font-weight:700; color:#8BEA6A; line-height:1.1;">10.0.0.2</div>
            <div style="margin-top:6px; color:#C0C7D1; font-size:0.9rem; line-height:1.2;">Enter the robot IP address</div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <div style="display:flex; align-items:center; justify-content:center; align-self:center; height:100%;">
    <div style="color:#8BEA6A; font-weight:700; text-align:center;">
      <div style="margin-bottom:10px;">Access</div>
      <div style="font-size:48px; line-height:1;">→</div>
    </div>
  </div>

  <div style="border:1px solid rgba(255,255,255,0.08); border-radius:18px; background:rgba(255,255,255,0.02); padding:18px; display:flex; flex-direction:column;">
    <div style="text-align:center; font-weight:700; margin-bottom:14px;">Robot Controller Screen</div>
    <div style="flex:1; min-height:250px; display:flex; align-items:center; justify-content:center;">
      <div style="width:100%; max-width:520px; height:250px; display:flex; align-items:center; justify-content:center; border:1px solid rgba(255,255,255,0.08); border-radius:14px; overflow:hidden; background:#11161d;">
        <img src="../images/browser-access-screen.png" alt="Robot controller screen" style="width:100%; height:100%; object-fit:contain; display:block;">
      </div>
    </div>
  </div>
</div>
