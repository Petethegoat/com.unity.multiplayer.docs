---  
id: Unity.Networking.Transport.Utilities.SimulatorUtility.Parameters  
title: Unity.Networking.Transport.Utilities.SimulatorUtility.Parameters  
---

<div class="markdown level0 summary">

Configuration parameters for the simulator pipeline stage.

</div>

<div class="markdown level0 conceptual">

</div>

<div classs="implements">

##### Implements

<div>

INetworkParameter

</div>

</div>

<div class="inheritedMembers">

##### Inherited Members

<div>

ValueType.Equals(Object)

</div>

<div>

ValueType.GetHashCode()

</div>

<div>

ValueType.ToString()

</div>

<div>

Object.Equals(Object, Object)

</div>

<div>

Object.GetType()

</div>

<div>

Object.ReferenceEquals(Object, Object)

</div>

</div>

##### **Namespace**: System.Dynamic.ExpandoObject

##### **Assembly**: transport.dll

##### Syntax

``` lang-csharp
public struct Parameters : INetworkParameter
```

## 

### FuzzFactor

<div class="markdown level1 summary">

Use the fuzz factor when you want to fuzz a packet. For every packet a
random number generator is used to determine if the packet should have
the internal bits flipped. A percentage of 5 means approximately every
20th packet will be fuzzed, and that each bit in the packet has a 5
percent chance to get flipped.

</div>

<div class="markdown level1 conceptual">

</div>

#### Declaration

``` lang-csharp
public int FuzzFactor
```

#### Field Value

| Type         | Description |
|--------------|-------------|
| System.Int32 |             |

### FuzzOffset

<div class="markdown level1 summary">

Use the fuzz offset in conjunction with the fuzz factor, the fuzz offset
will offset where we start flipping bits. This is useful if you want to
only fuzz a part of the packet.

</div>

<div class="markdown level1 conceptual">

</div>

#### Declaration

``` lang-csharp
public int FuzzOffset
```

#### Field Value

| Type         | Description |
|--------------|-------------|
| System.Int32 |             |

### MaxPacketCount

<div class="markdown level1 summary">

The maximum amount of packets the pipeline can keep track of. This used
when a packet is delayed, the packet is stored in the pipeline
processing buffer and can be later brought back.

</div>

<div class="markdown level1 conceptual">

</div>

#### Declaration

``` lang-csharp
public int MaxPacketCount
```

#### Field Value

| Type         | Description |
|--------------|-------------|
| System.Int32 |             |

### MaxPacketSize

<div class="markdown level1 summary">

The maximum size of a packet which the simulator stores. If a packet
exceeds this size it will bypass the simulator.

</div>

<div class="markdown level1 conceptual">

</div>

#### Declaration

``` lang-csharp
public int MaxPacketSize
```

#### Field Value

| Type         | Description |
|--------------|-------------|
| System.Int32 |             |

### PacketDelayMs

<div class="markdown level1 summary">

Fixed delay to apply to all packets which pass through.

</div>

<div class="markdown level1 conceptual">

</div>

#### Declaration

``` lang-csharp
public int PacketDelayMs
```

#### Field Value

| Type         | Description |
|--------------|-------------|
| System.Int32 |             |

### PacketDropInterval

<div class="markdown level1 summary">

Fixed interval to drop packets on. This is most suitable for tests where
predictable behaviour is desired, every Xth packet will be dropped. If
PacketDropInterval is 5 every 5th packet is dropped.

</div>

<div class="markdown level1 conceptual">

</div>

#### Declaration

``` lang-csharp
public int PacketDropInterval
```

#### Field Value

| Type         | Description |
|--------------|-------------|
| System.Int32 |             |

### PacketDropPercentage

<div class="markdown level1 summary">

Use a drop percentage when deciding when to drop packet. For every
packet a random number generator is used to determine if the packet
should be dropped or not. A percentage of 5 means approximately every
20th packet will be dropped.

</div>

<div class="markdown level1 conceptual">

</div>

#### Declaration

``` lang-csharp
public int PacketDropPercentage
```

#### Field Value

| Type         | Description |
|--------------|-------------|
| System.Int32 |             |

### PacketJitterMs

<div class="markdown level1 summary">

Variable delay to apply to all packets which pass through, adds or
subtracts amount from fixed delay.

</div>

<div class="markdown level1 conceptual">

</div>

#### Declaration

``` lang-csharp
public int PacketJitterMs
```

#### Field Value

| Type         | Description |
|--------------|-------------|
| System.Int32 |             |

### RandomSeed

<div class="markdown level1 summary">

The random seed is used to set the initial seed of the random number
generator. This is useful to get deterministic runs in tests for example
that are dependant on the random number generator.

</div>

<div class="markdown level1 conceptual">

</div>

#### Declaration

``` lang-csharp
public uint RandomSeed
```

#### Field Value

| Type          | Description |
|---------------|-------------|
| System.UInt32 |             |

### Implements

<div>

INetworkParameter

</div>
