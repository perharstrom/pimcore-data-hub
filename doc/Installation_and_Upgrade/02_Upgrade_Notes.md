# Upgrade Notes

## 1.6.0
- When using Pimcore 11 configurations from `datahub-configurations.php` are no longer used. To migrate those configurations
to the settings store, use the provided `datahub:configuration:migrate-legacy-config` command.
- Added the ability to import and export each type of data-hub configuration.
Be sure to include the `supported_types` configuration in any custom implementation to use the import functionality!

## 1.5.0
- When "Skip Permission Check" is active in a GraphQL configuration, the "Workspaces" settings are also skipped 
- It is possible to add more than one API-key per configuration now. Therefore, the API-key gets stored as an array
in the configuration. Configurations from previous versions are still supported, but they get converted to the new format
as soon as they get saved.
- Added "Translation Listing" and "Translation" to the Generic Types
