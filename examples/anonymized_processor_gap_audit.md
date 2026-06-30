# Example: Audio Processor Gap Audit

## Question

Can we prove which input currently feeds the on-air processor?

## Vendor documentation proves

- analog input capability;
- digital input capability;
- AoIP capability;
- backup/failover capability;
- presets and monitoring capability.

## Station evidence available

- device identity;
- management IP;
- manual mapping;
- official user manual.

## Station evidence missing

- exported configuration;
- active input status;
- active output status;
- current preset;
- alarm status;
- failover state.

## Correct conclusion

The processor capability is documented. The active on-air input is **unknown**.

## Safest next action

Request a read-only status export or approved read-only web UI observation.

## Incorrect conclusion to avoid

“The device is using AES67 because the manual supports AES67.”
