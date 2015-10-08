# Keychain-iOS-ObjC
Keychain-iOS-ObjC is a simple Objective-C wrapper for working with the Keychain in iOS, `KFKeychain` class is able to save, load and delete from iOS Keychain arbitrary objects, including, for example, `NSSString` and `NSDictionary`.

## Example

Let's assume that we want to store user authorization token in iOS keychain. In this case code might look like that:

```
- (void)saveAuthToken:(NSString *)authToken {
    [KFKeychain saveObject:authToken forKey:kUserAuthTokenKey];
}

- (NSString *)authToken {
    return [KFKeychain loadObjectForKey:kUserAuthTokenKey];
}

- (void)removeAuthToken {
    [KFKeychain deleteObjectForKey:kUserAuthTokenKey];
}
```

## Swift

For Swift version of this code please take a look at [Keychain-iOS-Swift](https://github.com/Keyflow/Keychain-iOS-Swift)

## License

This project is licensed under the terms of the MIT license.