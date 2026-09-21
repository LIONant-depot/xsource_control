# xsource_control

Source-control abstraction for editors: one workspace-session interface (`sc::IWorkspaceSession`) with a git + git-lfs
provider. Header-only, no dependency on any editor or UI.

| Path | Contents |
|---|---|
| `source/sc_iworkspace_session.hpp` | the interface and its value types (`sc::FileStatus`, `sc::LockInfo`, ...) |
| `source/sc_git_lfs_provider.hpp` | git + git-lfs implementation |
| `source/sc_process_runner.hpp` | child-process runner used by the provider |
| `documentation/` | the abstraction spec |
| `smoke/` | console smoke test for the provider |

`source/editor/` is where the editor-facing parts (commands, status cache, panel) belong; they currently live in
`xGPU/source/Examples/E29_LevelSceneEditor/extensions/source_control/` until they no longer depend on E29.
