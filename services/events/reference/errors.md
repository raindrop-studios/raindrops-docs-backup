# Errors

Errors are returned in hexadecimal format from the Solana Blockchain, convert to decimal then reference this page to determine the error. If the decimal returned is not a 6XXX number, then the error is a built-in error from the Solana blockchain, reference here to troubleshoot: [https://docs.rs/anchor-lang/latest/anchor\_lang/error/enum.ErrorCode.html](https://docs.rs/anchor-lang/latest/anchor\_lang/error/enum.ErrorCode.html)



```rust
// Event Name Length too long
// 6000
NameTooLong

// Event has Ended
// 6001
EventEnded

// Contest has Ended
// 6002
ContestEnded

// Invalid Index
// 6003
InvalidIndex

// Event is Full, no more participants can join
// 6004
EventFull

// Contest is Full, no more participants can join
// 6005
ContestFull

// Event Entry Fee Not Paid, must be paid in same transcation as JoinEvent
// 6006
EventEntryFeeNotPaid

// Participant Failed Event Token Gate Validation
// 6007
EventTokenGateValidationFailed

// Contest Entry Fee Not Paid, must be paid in same transcation as JoinContest
// 6008
ContestEntryFeeNotPaid

// Participant Failed Contest Token Gate Validation
// 6009
ContestTokenGateValidationFailed

// Event Not Ended, cannot distribute rewards
// 6010
EventNotEnded

// Event has Already Started, no more participants can join
// 6011
EventAlreadyStarted

// Contest has Already Started, no more participants can join
// 6012
ContestAlreadyStarted

// Contest has not finished, cannot distribute points
// 6013
ContestNotEnded

// Event has been finalized, no more changes allowed
// 6014
EventFinalized

// Contest has been finalized, no more changes allowed
// 6015
ContestFinalized

// Token Gate Check Failed
// 6016
TokenGateFailed

// Insufficient Permissions to Join Contest
// 6017
InsufficientJoinPermission
```
