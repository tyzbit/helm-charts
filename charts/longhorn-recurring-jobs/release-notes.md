# Breaking Changes

- The `parameters` key in any given group has been renamed `default`.

# Enhancements

- Allow specifying any task type (snapshot, backup, snapshot-cleanup, snapshot-delete and more).
  - For more info on the new task types, see the official [Longhorn documentation](https://longhorn.io/docs/1.4.1/snapshots-and-backups/scheduling-backups-and-snapshots/#set-up-recurring-jobs-using-a-longhorn-recurringjob)
  - Updated example in `values.yaml`.
- Add default retention with defaultRetain.

# Bugfixes

**None**
