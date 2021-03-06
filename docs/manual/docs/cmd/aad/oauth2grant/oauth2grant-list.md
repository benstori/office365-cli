# aad oauth2grant list

Lists OAuth2 permission grants for the specified service principal

## Usage

```sh
aad oauth2grant list [options]
```

## Options

Option|Description
------|-----------
`--help`|output usage information
`-i, --clientId <clientId>`|objectId of the service principal for which the configured OAuth2 permission grants should be retrieved
`-o, --output <output>`|Output type. `json|text`. Default `text`
`--verbose`|Runs command with verbose logging
`--debug`|Runs command with debug logging

!!! important
    Before using this command, connect to Azure Active Directory Graph, using the [aad connect](../connect.md) command.

## Remarks

To get information about service principal OAuth2 permission grants, you have to first connect to Azure Active Directory Graph using the [aad connect](../connect.md) command, eg. `aad connect`.

In order to list existing OAuth2 permissions granted to a service principal, you need its `objectId`. You can retrieve it using the [aad sp get](../sp/sp-get.md) command.

## Examples

List OAuth2 permissions granted to service principal with `objectId` _b2307a39-e878-458b-bc90-03bc578531d6_.

```sh
aad oauth2grant list --clientId b2307a39-e878-458b-bc90-03bc578531d6
```

## More information

- Application and service principal objects in Azure Active Directory (Azure AD): [https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-application-objects](https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-application-objects)