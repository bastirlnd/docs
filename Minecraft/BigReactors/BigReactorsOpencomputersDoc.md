# EnergyDevice Documentation
Documentation for energy_device types in OpenComputers\
EnergyDevices are called with `component.energy_device`

## Energy
- getEnergyStored()
Get currently stored amount of energy
`float = component.energy_device.getEnergyStored()`
- getMaxEnergyStored()
Returns maximum energy capacity in RF
`float = component.energy_device.getMaxEnergyStored()`
- canReceive()
Checks if device can receive energy
`boolean = component.energy_device.canReceive()`
- canExtract()
Checks if device can output energy
`boolean = component.energy_device.canExtract()`

## OpenComputers
- type
Returns oc-type of device
`string = component.energy_device.type`
- address
Returns oc-address of device
`string = component.energy_device.address`
- slot
Returns oc-slot of device
`int = component.energy_device.slot`

# BigReactors Documentation
This is an unofficial BigReactors Documentation for the mod OpenComputers\
All reactors are called with `component.br_reactor`

- help()
This method has not been implemented yet.

## MultiBlock
- mbIsConnected()
Haven found out what this does yet.
`boolean = component.br_reactor.mbIsConnected()`
- mbGetMultiblockControllerTypeName()
No idea
`string = component.br_reactor.mbGetMultiblockControllerTypeName()`
- mbIsPaused()
No idea
`boolean = component.br_reactor.mbIsPaused()`
- mbGetMinimumCoordinate()
No idea
`x, y, z = component.br_reactor.mbGetMinimumCoordinate()`
- mbGetMaximumCoordinate()
No idea
`x, y, z = component.br_reactor.mbGetMaximumCoordinate()`
- component.br_reactor.mbIsDisassembled()
Checks if reactor is disassembled
`boolean = component.br_reactor.mbIsDisassembled()`
- mbIsAssembled()
Checks if reactor is assembled
`boolean = component.br_reactor.mbIsAssembled()`

## Energy
- getEnergyStats()
It allows you to get all energy related stats in one command
`table = component.br_reactor.getEnergyStats()`
returned `table` contains:
-- `table.energyProducedLastTick`
-- `table.energyStored`
-- `table.energyCapacity`
- getEnergyStored()
Returns currently energy stored in the reactor
`float = component.br_reactor.getEnergyStored()`
- getEnergyProducedLastTick()
Returns energy produced last tick
`float = component.br_reactor.getEnergyProducedLastTick()`
- getEnergyCapacity()
Returns the max energy capacity of the reactor
`float = component.br_reactor.getEnergyCapacity()`

## Reactor
- getMultiblockAssembled()
Returns true of reactor is assembled
`bool = component.br_reactor.getMultiblockAssembled()`
- getMinimumCoordinate()
Returns first block on the lowest point of the reactor
`x, y, z = component.br_reactor.getMinimumCoordinate()`
- getActive()
Checks if reactor is running
`boolean = component.br_reactor.getActive()`
- setActive(bool active)
Activates or deactivates reactor
`component.br_reactor.setActive(boolean active)`
- getMaximumCoordinate()
Returns last block on the highest point of the reactor
`x, y, z = component.br_reactor.getMaximumCoordinate()`
- getConnected()
Checks if reactor is connected to computer network
`boolean = component.br_reactor.getConnected()`
- getCasingTemperature()
Gives you current casing temperature
`float = component.br_reactor.getCasingTemperature()`

## Control Rod

- setAllControlRodLevels()
Sets control rod levels for all rods equally
`component.br_reactor.setAllControlRodLevels(int percent)`
- getControlRodsLevels()
Gives you all control rod levels in a table
`table = component.br_reactor.getControlRodsLevels()`
- component.br_reactor.getControlRodLevel()
Gets control rod level of given rod number
`float = component.br_reactor.getControlRodLevel(int rod-number)`
- getControlRodName()
Gets name of given control rod number
`string = component.br_reactor.getControlRodName(int rod-number)`
- setControlRodLevel(int rod-id, int percent)
Set control rod level of given rod number
`component.br_reactor.setControlRodLevel(int rod-id, int percent)`
- component.br_reactor.setControlRodName()
Sets a name for specified control rod
`component.br_reactor.setControlRodName(int rod-id, string name)`
- getNumberOfControlRods()
Returns number of total control rods
`int = component.br_reactor.getNumberOfControlRods()`
- setControlRodLevel()
Set control rod percentage for given rod
`component.br_reactor.setControlRodLevel(int rod-id, int percent)`
- getControlRodLocation()
Returns location from given control rod
`x, y, z = component.br_reactor.getControlRodLocation(int rod-id)`

## Fuel

- getFuelTemperature()
Gets current fuel temperature
`float = component.br_reactor.getFuelTemperature()`
- getFuelComsumedLastTick()
Gets fuel consumtion from last tick
`float = component.br_reactor.getFuelComsumedLastTick()`
- getFuelAmountMax()
Returns max fuel amount in millibuckets
`float = component.br_reactor.getFuelAmountMax()`
- getFuelStats()
Allows you to get all fuel related stats in one command
`table = component.br_reactor.getFuelStats()`
returned `table` contains:
-- `table.fuelTemperature`
-- `table.fuelCapacity`
-- `table.fuelReactivity`
-- `table.fuelAmount`
-- `table.wasteAmount`
-- `table.fuelConsumedLastTick`
- getFuelAmount()
Returns stored fuel amount in millibuckets
`float = component.br_reactor.getFuelAmount()`
- getFuelReactivity()
Returns fuel reactivity in percent
`float = component.br_reactor.getFuelReactivity()`
- doEjectFuel()
Ejects fuel into reactor access ports
`component.br_reactor.doEjectFuel()`
- doEjectWaste()
Ejects waste if not automatically ejected
`component.br_reactor.doEjectWaste()`
- getWasteAmount()
Returns amount of waste inside the reactor in millibuckets
`float = component.br_reactor.getWasteAmount()`

## Cooling

- getHotFluidProducedLastTick()
Returns how much fluid has been produced last tick in millibuckets
`float = component.br_reactor.getHotFluidProducedLastTick()`
- isActivelyCooled()
Checks if reactor is actively cooled
`boolean = component.br_reactor.isActivelyCooled()`
- getCoolantType()
Returns fluid which is cooling the reactor
`string = component.br_reactor.getCoolantType()`
- getCoolantFluidStats()
Gets you all coolant fluid related stats
`table = component.br_reactor.getCoolantFluidStats()`
returned `table` contains:
-- `table.fluidCapacity`
-- `table.fluidAmount`
- getHotFluidType()
Returns which hot fluid is being produced
`string = component.br_reactor.getHotFluidType()`
- getHotFluidAmount()
Returns the amount of hot fluid in millibuckets
`float = component.br_reactor.getHotFluidAmount()`
- getHotFluidAmountMax()
Gets the maximum amount of hot fluid in millibuckets
`float = component.br_reactor.getHotFluidAmountMax()`
- getHotFluidStats()
Gets you all hot fluid related stats
`table = component.br_reactor.getHotFluidStats()`
returned `table` contains:
-- `table.fluidAmount`
-- `table.fluidProducedLastTick`
-- `table.fluidCapacity`
- getCoolantAmount()
Gets current amount of collant in the reactor in millibuckets
`float = component.br_reactor.getCoolantAmount()`
- getCoolantAmountMax()
Get the maximum amount of coolant in millibuckets
`float = component.br_reactor.getCoolantAmountMax()`

## OpenComputers
- address
Gets opencomputers-address of the reactor
`string = component.br_reactor.address`
- type
Returns oc-component type
`string = component.br_reactor.type`
- slot
Returns oc-slot
`int = component.br_reactor.slot`
- component.br_reactor.isMethodAvailable()
Checks if method is available
`boolean = component.br_reactor.isMethodAvailable(string fullnameofmethod)`