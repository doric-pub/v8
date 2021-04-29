# v8
Google V8 Engine Binary


# Windows V8 Build Info
commit 00afef3c7f78e4643f29721dc84286689b575e98 (HEAD, origin/master, origin/HEAD, master)
Author: Leszek Swirski <leszeks@chromium.org>
Date:   Tue Mar 30 13:18:36 2021 +0200

[sparkplug/ia32] Fix argc clobbering

Fix the InstallBaselineCode path in the InterpreterEntryTrampoline to
restore the clobbered eax (i.e. argc) register.

Bug: v8:11420, chromium:1192459
Change-Id: I97ce5739cf22a08fbb46dbf372ab6276bb802440
Reviewed-on: https://chromium-review.googlesource.com/c/v8/v8/+/2791567
Commit-Queue: Leszek Swirski <leszeks@chromium.org>
Commit-Queue: Victor Gomes <victorgomes@chromium.org>
Auto-Submit: Leszek Swirski <leszeks@chromium.org>
Reviewed-by: Victor Gomes <victorgomes@chromium.org>
Cr-Commit-Position: refs/heads/master@{#73721}

# macOS V8 Build Info
commit d0778a8d53eeff3ade42c24a03b34f2fe827aa9a (HEAD, origin/master, origin/HEAD, master)
Author: Dominik Inführ <dinfuehr@chromium.org>
Date:   Wed Mar 31 18:01:36 2021 +0200

[heap] Make stress_concurrent_allocation more resilient against OOM

Allow all allocations to fail in StressConcurrentAllocatorTask, this
still stresses the concurrent allocation code path but makes
--stress-concurrent-allocation more resilient against OOM. In case the
allocation fails try to start a GC.

Bug: v8:9337
Change-Id: I3633687d67d3a135114a3ea46b5238378153f377
Reviewed-on: https://chromium-review.googlesource.com/c/v8/v8/+/2797280
Reviewed-by: Ulan Degenbaev <ulan@chromium.org>
Commit-Queue: Dominik Inführ <dinfuehr@chromium.org>
Cr-Commit-Position: refs/heads/master@{#73802}

