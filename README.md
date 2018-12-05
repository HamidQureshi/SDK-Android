<img src="https://www.activeledger.io/wp-content/uploads/2018/09/Asset-23.png" alt="Activeledger" width="500"/>


# Activeledger SDK-Android

To use the Android SDK please Add it in your root build.gradle at the end of repositories:

```Java
allprojects {
	repositories {
		maven { url 'https://jitpack.io' }
	}
}
```

Add the dependency

```Java
dependencies {
	implementation 'com.github.activeledger:SDK-Android:Tag'
}
```

For Maven:

```Java
<repositories>
	<repository>
		<id>jitpack.io</id>
		<url>https://jitpack.io</url>
	</repository>
</repositories>
```

Add the dependency

```Java
<dependency>
	<groupId>com.github.activeledger</groupId>
	<artifactId>SDK-Android</artifactId>
	<version>Tag</version>
</dependency>
```

###NOTE: Please update the Tag : 0.1.1

## SDK Dev Instruction

Use the ActiveLedger SDK interface to Use the SDK.

## Initialise the SDK

```Java
ActiveLedgerSDK.getInstance().initSDK(this,"protocol","URL","port");
Example:
ActiveLedgerSDK.getInstance().initSDK(this,"http","testnet-uk.activeledger.io","5260");
```

## Generate KeyPair

```Java
KeyPair keyPair = ActiveLedgerSDK.getInstance().generateAndSetKeyPair(KeyType,SaveKeysToFile);
Example:
KeyPair keyPair = ActiveLedgerSDK.getInstance().generateAndSetKeyPair(keyType,true);
```

## Oboard KeyPair

```Java
ActiveLedgerSDK.getInstance().onBoardKeys(KeyPair, "KeyName");
Example:
ActiveLedgerSDK.getInstance().onBoardKeys(keyPair, "ActiveLedgerAwesomeKey");
```