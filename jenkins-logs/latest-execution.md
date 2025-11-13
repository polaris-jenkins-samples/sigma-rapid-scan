# Jenkins Execution Log

## Build Information
- **Job Name:** `MBP_Github_Polaris_Rapid_Scan/main`
- **Build Number:** #4
- **Build Status:** 🟢 **SUCCESS**
- **Duration:** 2 min 46 sec and counting
- **Timestamp:** 2025-11-13 11:52:33 UTC

---

## Console Output

```
Started by user admin
Connecting to https://api.github.com using madhusud@blackduck.com/****** (Github_Username_PAT)
Obtained nodejs-npm/Jenkinsfile from 2123a6e24e28f43ca417556841bf1498fc5d52e8
Loading library blackduck-logs-publisher@main
Attempting to resolve main from remote references...
 > git --version # timeout=10
 > git --version # 'git version 2.39.5 (Apple Git-154)'
using GIT_ASKPASS to set credentials Github_Username_PAT
 > git ls-remote -h -- https://github.com/integrations-garage/blackduck-logs-publisher # timeout=10
Found match: refs/heads/main revision e969196a63b1be83b84541b022f7aa52928bd5e5
The recommended git tool is: NONE
using credential Github_Username_PAT
 > git rev-parse --resolve-git-dir /Users/madhusud/.jenkins/workspace/P_Github_Polaris_Rapid_Scan_main@libs/a0dda568bac7bbb4a171f59ba3f2660c21c69edc6356524e9ae8bb4500c12bbb/.git # timeout=10
Fetching changes from the remote Git repository
 > git config remote.origin.url https://github.com/integrations-garage/blackduck-logs-publisher # timeout=10
Fetching without tags
Fetching upstream changes from https://github.com/integrations-garage/blackduck-logs-publisher
 > git --version # timeout=10
 > git --version # 'git version 2.39.5 (Apple Git-154)'
using GIT_ASKPASS to set credentials Github_Username_PAT
 > git fetch --no-tags --force --progress -- https://github.com/integrations-garage/blackduck-logs-publisher +refs/heads/*:refs/remotes/origin/* # timeout=10
Checking out Revision e969196a63b1be83b84541b022f7aa52928bd5e5 (main)
 > git config core.sparsecheckout # timeout=10
 > git checkout -f e969196a63b1be83b84541b022f7aa52928bd5e5 # timeout=10
Commit message: "Phase 3 - 2"
 > git rev-list --no-walk e969196a63b1be83b84541b022f7aa52928bd5e5 # timeout=10
[Pipeline] Start of Pipeline
[Pipeline] node
Running on mac-sh in /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main
[Pipeline] {
[Pipeline] stage
[Pipeline] { (Declarative: Checkout SCM)
[Pipeline] checkout
The recommended git tool is: NONE
using credential Github_Username_PAT
Fetching changes from the remote Git repository
Fetching without tags
 > git rev-parse --resolve-git-dir /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/.git # timeout=10
 > git config remote.origin.url https://github.com/polaris-jenkins-samples/sigma-rapid-scan.git # timeout=10
Fetching upstream changes from https://github.com/polaris-jenkins-samples/sigma-rapid-scan.git
 > git --version # timeout=10
 > git --version # 'git version 2.39.5 (Apple Git-154)'
using GIT_ASKPASS to set credentials Github_Username_PAT
 > git fetch --no-tags --force --progress -- https://github.com/polaris-jenkins-samples/sigma-rapid-scan.git +refs/heads/main:refs/remotes/origin/main # timeout=10
Checking out Revision 2123a6e24e28f43ca417556841bf1498fc5d52e8 (main)
Commit message: "Polaris Rapid Scan"
 > git config core.sparsecheckout # timeout=10
 > git checkout -f 2123a6e24e28f43ca417556841bf1498fc5d52e8 # timeout=10
 > git rev-list --no-walk 86be7ad3cda3dc3d8fe81948d641795fb4396f87 # timeout=10
[Pipeline] }
[Pipeline] // stage
[Pipeline] withEnv
[Pipeline] {
[Pipeline] stage
[Pipeline] { (Build)
[Pipeline] script
[Pipeline] {
[Pipeline] echo
JOB_NAME: MBP_Github_Polaris_Rapid_Scan/main
[Pipeline] dir
Running in /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm
[Pipeline] {
[Pipeline] sh
+ node --version
v22.16.0
[Pipeline] sh
+ npm --version
10.9.2
[Pipeline] sh
+ npm install
npm warn deprecated fsevents@1.2.9: fsevents 1 will break on node v14+ and could be using insecure binaries. Upgrade to fsevents 2.

up to date, audited 1412 packages in 5s

32 packages are looking for funding
  run `npm fund` for details

137 vulnerabilities (9 low, 35 moderate, 57 high, 36 critical)

To address issues that do not require attention, run:
  npm audit fix

To address all issues possible (including breaking changes), run:
  npm audit fix --force

Some issues need review, and may require choosing
a different dependency.

Run `npm audit` for details.
[Pipeline] }
[Pipeline] // dir
[Pipeline] }
[Pipeline] // script
[Pipeline] }
[Pipeline] // stage
[Pipeline] stage
[Pipeline] { (polaris-rapid-scan)
[Pipeline] script
[Pipeline] {
[Pipeline] dir
Running in /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm
[Pipeline] {
[Pipeline] security_scan
WARNING: Unknown parameter(s) found for class type 'io.jenkins.plugins.security.scan.extension.pipeline.SecurityScanStep': polaris_test_sast_type
**************************** START EXECUTION OF BLACK DUCK SECURITY SCAN ****************************
[Security Scan] INFO: Jenkins Job name: MBP_Github_Polaris_Rapid_Scan
-------------------------------- Connection to node --------------------------------
[Security Scan] INFO: Jenkins job is running on agent node remotely
-------------------------- Parameter Validation Initiated --------------------------
[Security Scan] INFO:  --- product = [POLARIS]
[Security Scan] INFO: Parameters for polaris:
[Security Scan] INFO:  --- polaris_waitForScan = true
[Security Scan] INFO:  --- polaris_server_url = https://poc.polaris.blackduck.com
[Security Scan] INFO:  --- polaris_assessment_types = SAST,SCA
[Security Scan] INFO:  --- polaris_access_token = ******************************************************************************
------------------------------------------------------------------------------------
[Security Scan] INFO: Parameters for additional configuration:
[Security Scan] INFO:  --- network_airgap = false
[Security Scan] INFO: Polaris parameters are validated successfully
[Security Scan] INFO: Bridge download parameters are validated successfully
[Security Scan] INFO: Bridge download is not required. Found installed in: /Users/madhusud/bridge-cli-bundle/bridge-cli-bundle-macos_arm
------------------------------------------------------------------------------------
[Security Scan] INFO: Bridge CLI version is - 3.9.2
[Security Scan] INFO: Jenkins Job name: MBP_Github_Polaris_Rapid_Scan
[Security Scan] INFO: Polaris Application Name: sigma-rapid-scan
[Security Scan] INFO: Polaris Project Name: sigma-rapid-scan
[Security Scan] INFO: Polaris Branch Name: main
[Security Scan] INFO: Jenkins Job name: MBP_Github_Polaris_Rapid_Scan
[Security Scan] INFO: Executable command line arguments: /Users/madhusud/bridge-cli-bundle/bridge-cli-bundle-macos_arm/bridge-cli --stage polaris --input /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/polaris_input12219999467298383140.json --out .bridge/output/scan_info_out.json

******************************* START EXECUTION OF BRIDGE CLI *******************************
2025-11-13 11:50:05.0338 IST [Bridge CLI] INFO: Using cache directory: /Users/madhusud/bridge-cli-bundle/bridge-cli-bundle-macos_arm
2025-11-13 11:50:05.0480 IST [Bridge CLI] INFO: Found version "3.0.371" in registry for workflow "polaris", trying to load it from local cache
2025-11-13 11:50:06.3774 IST [Bridge CLI] INFO: Input Resources:
2025-11-13 11:50:06.3774 IST [Bridge CLI] INFO: resource = value [source]
2025-11-13 11:50:06.3775 IST [Bridge CLI] INFO: ------------------------------------------------------------
2025-11-13 11:50:06.3775 IST [Bridge CLI] INFO: network.airgap = false [polaris_input12219999467298383140.json]
2025-11-13 11:50:06.3775 IST [Bridge CLI] INFO: polaris.accesstoken = ***************************************** [polaris_input12219999467298383140.json]
2025-11-13 11:50:06.3775 IST [Bridge CLI] INFO: polaris.application.name = sigma-rapid-scan [polaris_input12219999467298383140.json]
2025-11-13 11:50:06.3775 IST [Bridge CLI] INFO: polaris.assessment.types = [SAST SCA] [polaris_input12219999467298383140.json]
2025-11-13 11:50:06.3775 IST [Bridge CLI] INFO: polaris.branch.name = main [polaris_input12219999467298383140.json]
2025-11-13 11:50:06.3775 IST [Bridge CLI] INFO: polaris.project.name = sigma-rapid-scan [polaris_input12219999467298383140.json]
2025-11-13 11:50:06.3775 IST [Bridge CLI] INFO: polaris.serverUrl = https://poc.polaris.blackduck.com [polaris_input12219999467298383140.json]
2025-11-13 11:50:06.3776 IST [Bridge CLI] INFO: polaris.waitForScan = true [polaris_input12219999467298383140.json]
2025-11-13 11:50:06.3776 IST [Bridge CLI] INFO: ------------------------------------------------------------
2025-11-13 11:50:06.3776 IST [Bridge CLI] INFO: Starting adapters for stage polaris
2025-11-13 11:50:06.3792 IST [Bridge CLI] INFO: Starting Adapter: Polaris Status Provider
2025-11-13 11:50:06.3792 IST [Bridge CLI] INFO: Starting Adapter: Polaris SCM Discovery
2025-11-13 11:50:06.3792 IST [Bridge CLI] INFO: Starting Adapter: Polaris Controller
2025-11-13 11:50:06.3792 IST [Bridge CLI] INFO: Starting Adapter: Polaris Initializer
2025-11-13 11:50:06.4519 IST [Polaris SCM Discovery] INFO: Adapter finished
2025-11-13 11:50:06.4557 IST [Bridge CLI] INFO: Starting Adapter: Set Polaris Assessment Mode to CI
2025-11-13 11:50:06.4558 IST [Set Polaris Assessment Mode to CI] INFO: Provided value for resource 'polaris.assessment.mode'
2025-11-13 11:50:06.4559 IST [Set Polaris Assessment Mode to CI] INFO: Adapter finished
2025-11-13 11:50:06.4589 IST [Bridge CLI] INFO: Starting Adapter: Create Polaris Project & Branch By Default
2025-11-13 11:50:06.4590 IST [Create Polaris Project & Branch By Default] INFO: Provided value for resource 'polaris.onboarding'
2025-11-13 11:50:06.4591 IST [Create Polaris Project & Branch By Default] INFO: Adapter finished
2025-11-13 11:50:08.5614 IST [Polaris Initializer] INFO: Successfully created test for "SCA(scaPackage)" assessment. The short test ID is "HRF8DDI"
2025-11-13 11:50:08.5614 IST [Polaris Initializer] INFO: Successfully created test for "SAST(sastFull)" assessment. The short test ID is "IV0U1FV"
2025-11-13 11:50:08.5878 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.test.SAST.tests.sastFull.id'
2025-11-13 11:50:08.5882 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.test.SCA.tests.scaPackage.id'
2025-11-13 11:50:08.5886 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.test.SAST.tests.sastFull.shortId'
2025-11-13 11:50:08.5896 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.test.SCA.tests.scaPackage.shortId'
2025-11-13 11:50:08.5899 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.test.SAST.tests.sastFull.streamId'
2025-11-13 11:50:08.5902 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.project.id'
2025-11-13 11:50:08.5905 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.branch.id'
2025-11-13 11:50:08.5907 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.portfolioid'
2025-11-13 11:50:08.5910 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.tenant.id'
2025-11-13 11:50:08.5913 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.application.id'
2025-11-13 11:50:08.5920 IST [Polaris Initializer] INFO: Adapter finished
2025-11-13 11:50:08.6120 IST [Bridge CLI] INFO: Starting Adapter: Check pull request
2025-11-13 11:50:08.6568 IST [Check pull request] INFO: Provided value for resource 'environment.scan.pull'
2025-11-13 11:50:08.6569 IST [Check pull request] INFO: Adapter finished
2025-11-13 11:50:08.6992 IST [Polaris Controller] INFO: Running for "sast" assessment with scan type "sastFull"
2025-11-13 11:50:08.6995 IST [Polaris Controller] INFO: fetching recommended "coverity" tool info...
2025-11-13 11:50:09.0415 IST [Polaris Controller] INFO: checking "coverity" tool installation inside bridge home directory: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0
2025-11-13 11:50:09.0416 IST [Polaris Controller] INFO: Checking tool version for "cov_thin_client" in "/Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0"
2025-11-13 11:50:09.0436 IST [Polaris Controller] INFO: Running command:/Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/coverity --version
2025-11-13 11:50:09.1240 IST [Polaris Controller] INFO: Got tool version for "cov_thin_client": 2025.9.0
2025-11-13 11:50:09.4241 IST [Polaris Controller] INFO: "coverity" tool is already installed...
2025-11-13 11:50:09.4243 IST [Polaris Controller] INFO: fetching recommended "Sigma" tool info...
2025-11-13 11:50:09.7197 IST [Polaris Controller] INFO: checking "Sigma" tool installation inside bridge home directory: /Users/madhusud/.blackduck/bridge/tools/sigma/2025.10.0
2025-11-13 11:50:09.7199 IST [Polaris Controller] INFO: Checking tool version for "sigma" in "/Users/madhusud/.blackduck/bridge/tools/sigma/2025.10.0"
2025-11-13 11:50:09.7201 IST [Polaris Controller] INFO: Running command:/Users/madhusud/.blackduck/bridge/tools/sigma/2025.10.0/sigma --version
2025-11-13 11:50:09.8043 IST [Polaris Controller] INFO: Got tool version for "sigma": 2025.10.0
2025-11-13 11:50:10.1044 IST [Polaris Controller] INFO: "Sigma" tool is already installed...
2025-11-13 11:50:10.1046 IST [Polaris Controller] INFO: Running for "sca" assessment with scan type "scaPackage"
2025-11-13 11:50:10.1047 IST [Polaris Controller] INFO: fetching recommended "detect" tool info...
2025-11-13 11:50:10.3975 IST [Polaris Controller] INFO: checking "detect" tool installation inside bridge home directory: /Users/madhusud/.blackduck/bridge/tools/blackduck-detect/10.4.0
2025-11-13 11:50:10.3977 IST [Polaris Controller] INFO: Running command:/Library/Java/JavaVirtualMachines/jdk-21.jdk/Contents/Home/bin/java -version
2025-11-13 11:50:10.4899 IST [Polaris Controller] INFO: Checking tool version for "detect" in "/Users/madhusud/.blackduck/bridge/tools/blackduck-detect/10.4.0"
2025-11-13 11:50:10.4937 IST [Polaris Controller] INFO: Got tool version for "detect": 10.4.0
2025-11-13 11:50:10.7849 IST [Polaris Controller] INFO: "detect" tool is already installed...
2025-11-13 11:50:10.8110 IST [Polaris Controller] INFO: Provided value for resource 'coverity.id'
2025-11-13 11:50:10.8112 IST [Polaris Controller] INFO: Provided value for resource 'sigma.id'
2025-11-13 11:50:10.8115 IST [Polaris Controller] INFO: Provided value for resource 'detect.id'
2025-11-13 11:50:10.8116 IST [Bridge CLI] INFO: Starting adapters for stage polaris-sast
2025-11-13 11:50:10.8116 IST [Bridge CLI] INFO: Starting adapters for stage polaris-sca-package
2025-11-13 11:50:10.8116 IST [Bridge CLI] INFO: Starting adapters for stage polaris-artifacts-uploader
2025-11-13 11:50:10.8116 IST [Bridge CLI] INFO: Starting adapters for stage polaris-post-processing
2025-11-13 11:50:10.8137 IST [Bridge CLI] INFO: Starting Adapter: Polaris SCA Package Manager Scan
2025-11-13 11:50:10.8137 IST [Bridge CLI] INFO: Starting Adapter: Polaris Coverity Capture
2025-11-13 11:50:10.8137 IST [Bridge CLI] INFO: Starting Adapter: Polaris Artifacts Uploader
2025-11-13 11:50:10.8137 IST [Bridge CLI] INFO: Starting Adapter: Polaris Waiter
2025-11-13 11:50:10.8137 IST [Bridge CLI] INFO: Starting Adapter: Polaris Issues Fetcher
2025-11-13 11:50:10.8137 IST [Bridge CLI] INFO: Starting Adapter: Polaris Policy Checker
2025-11-13 11:50:10.8144 IST [Polaris Controller] INFO: Adapter finished
2025-11-13 11:50:10.8493 IST [Bridge CLI] INFO: Starting Adapter: Default Adapter for execution path
2025-11-13 11:50:10.8503 IST [Default Adapter for execution path] INFO: Provided value for resource 'coverity.execution.path'
2025-11-13 11:50:10.8503 IST [Default Adapter for execution path] INFO: Adapter finished
2025-11-13 11:50:10.8570 IST [Bridge CLI] INFO: Starting Adapter: Default Adapter for execution path
2025-11-13 11:50:10.8571 IST [Default Adapter for execution path] INFO: Provided value for resource 'sigma.execution.path'
2025-11-13 11:50:10.8571 IST [Default Adapter for execution path] INFO: Adapter finished
2025-11-13 11:50:10.9132 IST [Polaris Coverity Capture] INFO: Identified workflow: Polaris
2025-11-13 11:50:10.9138 IST [Polaris Coverity Capture] INFO: command: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/coverity capture --dir /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir -o analyze.location=connect
2025-11-13 11:50:10.9733 IST [Polaris Coverity Capture] INFO: coverity 2025.9.0 covcli-2025.9-push-12
2025-11-13 11:50:10.9734 IST [Polaris Coverity Capture] INFO: envvar: COVERITY_CACHE_API_TOKEN_FILE=/var/folders/wm/gkd75sk54h57yqd0_j95gp2r0000gn/T/polaris_coverity_cache374283369/.authKey
2025-11-13 11:50:10.9734 IST [Polaris Coverity Capture] INFO: envvar: COVERITY_CACHE_KEY=0f728aa5-75c2-4d3b-ab7d-40c430569b85
2025-11-13 11:50:10.9734 IST [Polaris Coverity Capture] INFO: envvar: COVERITY_CACHE_URL=https://poc.polaris.blackduck.com/api/cache
2025-11-13 11:50:10.9734 IST [Polaris Coverity Capture] INFO: envvar: COVERITY_CLI_CAPTURE_ZIP_ARCHIVE=/Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/idir.zip
2025-11-13 11:50:10.9735 IST [Polaris Coverity Capture] INFO: envvar: COVERITY_CLI_POLARIS_CLIENT=true
2025-11-13 11:50:10.9747 IST [Polaris Coverity Capture] INFO: Detected that stdout is not connected to a terminal.  Defaulting ticker mode to 'none'.
2025-11-13 11:50:10.9747 IST [Polaris Coverity Capture] INFO: If this is not correct, explicitly set the ticker mode to the desired value using the '--ticker-mode' option.
2025-11-13 11:50:10.9756 IST [Polaris Coverity Capture] INFO: Executing command: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-manage-emit --dir /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir create
2025-11-13 11:50:11.0379 IST [Polaris Coverity Capture] INFO: Using lightweight capture with thin client.
2025-11-13 11:50:11.0382 IST [Polaris Coverity Capture] INFO: Executing command: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-internal-manage-cache check
2025-11-13 11:50:11.5580 IST [Polaris Coverity Capture] INFO: Caching is enabled.
2025-11-13 11:50:11.5606 IST [Polaris Coverity Capture] INFO: Telemetry is enabled
2025-11-13 11:50:12.2155 IST [Polaris Coverity Capture] INFO: Executing command: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-manage-emit --dir /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir list-capture-diagnostics
2025-11-13 11:50:12.2294 IST [Polaris Coverity Capture] INFO: Executing action no-op: nothing to do for initialization
2025-11-13 11:50:12.6484 IST [Polaris Coverity Capture] INFO: Executing action Delete compiler configurations for intermediate directory '/Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir'
2025-11-13 11:50:12.6486 IST [Polaris Coverity Capture] INFO: Executing action Configure build compiler: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-configure -c /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir/coverity-cli/build-compiler-configs/coverity_config.xml --compiler gcc --comptype clangcc --template
2025-11-13 11:50:12.9061 IST [Polaris Coverity Capture] INFO: Executing action Configure build compiler: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-configure -c /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir/coverity-cli/build-compiler-configs/coverity_config.xml --compiler cc --comptype gcc --template
2025-11-13 11:50:13.1242 IST [Polaris Coverity Capture] INFO: Executing action Configure build compiler: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-configure -c /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir/coverity-cli/build-compiler-configs/coverity_config.xml --compiler c++ --comptype g++ --template
2025-11-13 11:50:13.3601 IST [Polaris Coverity Capture] INFO: Executing action Configure build compiler: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-configure -c /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir/coverity-cli/build-compiler-configs/coverity_config.xml --compiler clang --comptype clangcc --template
2025-11-13 11:50:13.5832 IST [Polaris Coverity Capture] INFO: Executing action Configure build compiler: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-configure -c /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir/coverity-cli/build-compiler-configs/coverity_config.xml --compiler java --comptype java --template
2025-11-13 11:50:13.8119 IST [Polaris Coverity Capture] INFO: Executing action Configure build compiler: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-configure -c /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir/coverity-cli/build-compiler-configs/coverity_config.xml --compiler go --comptype go --template
2025-11-13 11:50:14.0489 IST [Polaris Coverity Capture] INFO: Executing action Configure build compiler: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-configure -c /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir/coverity-cli/build-compiler-configs/coverity_config.xml --compiler ccache --comptype prefix --template
2025-11-13 11:50:14.2787 IST [Polaris Coverity Capture] INFO: Executing action Configure build compiler: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-configure -c /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir/coverity-cli/build-compiler-configs/coverity_config.xml --compiler kotlinc --comptype kotlinc --template
2025-11-13 11:50:14.4979 IST [Polaris Coverity Capture] WARNING: Template config template-java-config-0 already exists for java and will be reused. 
2025-11-13 11:50:14.4979 IST [Polaris Coverity Capture] WARNING: Template config template-apt-config-0 already exists for apt and will be reused. 
2025-11-13 11:50:14.4979 IST [Polaris Coverity Capture] WARNING: Template config template-javaw-config-0 already exists for javaw and will be reused. 
2025-11-13 11:50:14.5024 IST [Polaris Coverity Capture] INFO: Executing action Configure build compiler: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-configure -c /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir/coverity-cli/buildless-compiler-configs/coverity_config.xml --dart
2025-11-13 11:50:14.7367 IST [Polaris Coverity Capture] INFO: Executing action Configure build compiler: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-configure -c /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir/coverity-cli/buildless-compiler-configs/coverity_config.xml --javascript
2025-11-13 11:50:14.9651 IST [Polaris Coverity Capture] INFO: Executing action Configure build compiler: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-configure -c /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir/coverity-cli/buildless-compiler-configs/coverity_config.xml --php
2025-11-13 11:50:15.1928 IST [Polaris Coverity Capture] INFO: Executing action Configure build compiler: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-configure -c /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir/coverity-cli/buildless-compiler-configs/coverity_config.xml --python
2025-11-13 11:50:15.4219 IST [Polaris Coverity Capture] INFO: Executing action Configure build compiler: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-configure -c /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir/coverity-cli/buildless-compiler-configs/coverity_config.xml --ruby
2025-11-13 11:50:15.6519 IST [Polaris Coverity Capture] INFO: Executing action Configure build compiler: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-configure -c /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir/coverity-cli/buildless-compiler-configs/coverity_config.xml --comptype capture-config-files --file-regex $capture-config-files$ --template
2025-11-13 11:50:15.6692 IST [Polaris Coverity Capture] WARNING: Configuration already exists for file regex $capture-config-files$
2025-11-13 11:50:15.6692 IST [Polaris Coverity Capture] INFO:           and it will not be updated.
2025-11-13 11:50:16.1092 IST [Polaris Coverity Capture] INFO: Executing action no-op: no compilers need to be unconfigured
2025-11-13 11:50:16.5099 IST [Polaris Coverity Capture] INFO: Executing action no-op: compiler configurations loaded
2025-11-13 11:50:17.0351 IST [Polaris Coverity Capture] INFO: Executing action Emit files using buildless capture: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-internal-capture-files --dir /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir -c /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir/coverity-cli/buildless-compiler-configs/coverity_config.xml --ticker-mode none --append-log --capture-list-file /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir/coverity-cli/capture-file-list-3163068939 --record-with-source
2025-11-13 11:50:17.0600 IST [Polaris Coverity Capture] INFO: Buildless capture started.
2025-11-13 11:50:17.0727 IST [Polaris Coverity Capture] INFO: Emitting 84 Files.
2025-11-13 11:50:17.5430 IST [Polaris Coverity Capture] INFO: Buildless capture completed.
2025-11-13 11:50:17.5447 IST [Polaris Coverity Capture] INFO: Executing action No unwanted TUs to delete
2025-11-13 11:50:17.5447 IST [Polaris Coverity Capture] INFO: Executing action Action cleanup: Unwanted TUs action cleanup
2025-11-13 11:50:17.5448 IST [Polaris Coverity Capture] INFO: Executing action deleteResidualTUs /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir
2025-11-13 11:50:17.5450 IST [Polaris Coverity Capture] INFO: Executing command: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-manage-emit --dir /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir list-capture-diagnostics
2025-11-13 11:50:17.5641 IST [Polaris Coverity Capture] INFO: Executing action Invalidate capture results
2025-11-13 11:50:17.5642 IST [Polaris Coverity Capture] INFO: Executing action Invoke cov-run-sigma: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-run-sigma --project-dir /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm --dir /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir --coverity-config /var/folders/wm/gkd75sk54h57yqd0_j95gp2r0000gn/T/cov-run-sigma-config-3245375468/coverity.yaml --sigma-binary-path /Users/madhusud/.blackduck/bridge/tools/sigma/2025.10.0/sigma --enable-telemetry
2025-11-13 11:50:17.5931 IST [Polaris Coverity Capture] INFO: cov-run-sigma version 2025.9.0 on Darwin 24.6.0 arm64
2025-11-13 11:50:17.5931 IST [Polaris Coverity Capture] INFO: Internal version numbers: 477d3c5ddd p-2025.9-push-57
2025-11-13 11:50:17.5931 IST [Polaris Coverity Capture] INFO: 
2025-11-13 11:50:19.2579 IST [Polaris Coverity Capture] INFO: Executing action Action cleanup: Coverity configuration for Sigma
2025-11-13 11:50:19.8350 IST [Polaris Coverity Capture] INFO: Executing command: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-manage-emit --dir /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir list-capture-diagnostics
2025-11-13 11:50:19.9054 IST [Polaris Coverity Capture] INFO: Capture summary:
2025-11-13 11:50:19.9055 IST [Polaris Coverity Capture] INFO:     SUCCEEDED: 87
2025-11-13 11:50:19.9055 IST [Polaris Coverity Capture] INFO:     INCOMPLETE: 0
2025-11-13 11:50:19.9055 IST [Polaris Coverity Capture] INFO:     FAILED: 0
2025-11-13 11:50:19.9055 IST [Polaris Coverity Capture] INFO:     IGNORED: 3
2025-11-13 11:50:19.9055 IST [Polaris Coverity Capture] INFO:     FILES CAPTURED: 87
2025-11-13 11:50:19.9055 IST [Polaris Coverity Capture] INFO:     LINES OF CODE: 32920
2025-11-13 11:50:19.9080 IST [Polaris Coverity Capture] INFO: Capture phase took 8.35s.
2025-11-13 11:50:19.9080 IST [Polaris Coverity Capture] WARNING: !! SOURCES FOR UNSUPPORTED LANGUAGES WERE DETECTED !!
2025-11-13 11:50:19.9080 IST [Polaris Coverity Capture] WARNING: 
2025-11-13 11:50:19.9081 IST [Polaris Coverity Capture] WARNING: Source files for the following languages were detected, but these languages are not supported on Mac OS ARM:
2025-11-13 11:50:19.9081 IST [Polaris Coverity Capture] WARNING:   * C#
2025-11-13 11:50:19.9081 IST [Polaris Coverity Capture] WARNING: In order to analyze these files, please analyze the project on an operating system and architecture where they are supported.
2025-11-13 11:50:19.9322 IST [Polaris Coverity Capture] INFO: To analyze your project, type '/Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/coverity analyze --dir /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir -o analyze.location=connect'.
2025-11-13 11:50:19.9339 IST [Polaris Coverity Capture] INFO: Coverity Capture completed successfully
2025-11-13 11:50:19.9405 IST [Polaris Coverity Capture] INFO: Provided value for resource 'coverity.completed'
2025-11-13 11:50:19.9406 IST [Polaris Coverity Capture] INFO: Provided value for resource 'coverity.idir.output'
2025-11-13 11:50:19.9408 IST [Polaris Coverity Capture] INFO: Provided value for resource 'polaris.test.sast.tests.sastFull.artifacts.path'
2025-11-13 11:50:19.9410 IST [Polaris Coverity Capture] INFO: Adapter finished
2025-11-13 11:50:19.9429 IST [Bridge CLI] INFO: Starting Adapter: Default Adapter for execution path
2025-11-13 11:50:19.9430 IST [Default Adapter for execution path] INFO: Provided value for resource 'detect.execution.path'
2025-11-13 11:50:19.9431 IST [Default Adapter for execution path] INFO: Adapter finished
2025-11-13 11:50:19.9762 IST [Polaris SCA Package Manager Scan] INFO: Running command /Library/Java/JavaVirtualMachines/jdk-21.jdk/Contents/Home/bin/java -jar /Users/madhusud/.blackduck/bridge/tools/blackduck-detect/10.4.0/detect-10.4.0.jar --detect.cleanup=false --detect.bdio.file.name=scan --detect.bdio.output.path=/Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/detect/bdio/blackduck_artifact --detect.output.path=/Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/detect --detect.tools=DETECTOR --detect.component.location.analysis.enabled=true --blackduck.offline.mode=true --blackduck.offline.mode.force.bdio=true
2025-11-13 11:50:20.0000 IST [Polaris SCA Package Manager Scan][main] WARNING: --- Detect-Self-Updater:  Self-Update feature is disabled because of the following reasons:
2025-11-13 11:50:20.0000 IST [Polaris SCA Package Manager Scan][main] WARNING: --- Detect-Self-Updater:  Detect in offline mode is incompatible with the Self-Update feature.
2025-11-13 11:50:20.0000 IST [Polaris SCA Package Manager Scan][main] WARNING: --- Detect-Self-Updater:  Black Duck URL is required for the Self-Update feature.
2025-11-13 11:50:20.7258 IST [Polaris SCA Package Manager Scan] INFO: ______     _            _
2025-11-13 11:50:20.7258 IST [Polaris SCA Package Manager Scan] INFO: |  _  \   | |          | |
2025-11-13 11:50:20.7259 IST [Polaris SCA Package Manager Scan] INFO: | | | |___| |_ ___  ___| |_
2025-11-13 11:50:20.7259 IST [Polaris SCA Package Manager Scan] INFO: | | | / _ \ __/ _ \/ __| __|
2025-11-13 11:50:20.7259 IST [Polaris SCA Package Manager Scan] INFO: | |/ /  __/ ||  __/ (__| |_
2025-11-13 11:50:20.7259 IST [Polaris SCA Package Manager Scan] INFO: |___/ \___|\__\___|\___|\__|
2025-11-13 11:50:20.7259 IST [Polaris SCA Package Manager Scan] INFO: 
2025-11-13 11:50:20.8545 IST [Polaris SCA Package Manager Scan] INFO: 
2025-11-13 11:50:20.8545 IST [Polaris SCA Package Manager Scan] INFO: Detect Version: 10.4.0
2025-11-13 11:50:20.8545 IST [Polaris SCA Package Manager Scan] INFO: 
2025-11-13 11:50:20.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 11:50:20.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Current property values:
2025-11-13 11:50:20.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- --property = value [notes]
2025-11-13 11:50:20.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ------------------------------------------------------------
2025-11-13 11:50:20.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- blackduck.offline.mode = true [cmd] 
2025-11-13 11:50:20.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- blackduck.offline.mode.force.bdio = true [cmd] 
2025-11-13 11:50:20.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- detect.bdio.file.name = scan [cmd] 
2025-11-13 11:50:20.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- detect.bdio.output.path = /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/detect/bdio/blackduck_artifact [cmd] 
2025-11-13 11:50:20.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- detect.cleanup = false [cmd] 
2025-11-13 11:50:20.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- detect.component.location.analysis.enabled = true [cmd] 
2025-11-13 11:50:20.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- detect.excluded.directories = /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge [env] 
2025-11-13 11:50:20.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- detect.output.path = /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/detect [cmd] 
2025-11-13 11:50:20.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- detect.tools = DETECTOR [cmd] 
2025-11-13 11:50:20.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ------------------------------------------------------------
2025-11-13 11:50:20.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 11:50:20.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Detect build date: 2025-04-24
2025-11-13 11:50:20.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Source directory: /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm
2025-11-13 11:50:20.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Output directory: /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/detect
2025-11-13 11:50:20.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Run directory: /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/detect/runs/2025-11-13-06-20-20-813
2025-11-13 11:50:20.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 11:50:21.0000 IST [Polaris SCA Package Manager Scan][main] WARNING: --- Correlated Scanning is not available for Rapid/Stateless scan mode or offline scanning. A correlation ID will not be set.
2025-11-13 11:50:21.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 11:50:21.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Docker tool will not be run.
2025-11-13 11:50:21.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 11:50:21.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Bazel tool will not be run.
2025-11-13 11:50:21.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 11:50:21.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Will include the Detectors tool.
2025-11-13 11:50:21.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Searching for detectors.
2025-11-13 11:50:21.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Evaluating detectors. This may take a while.
2025-11-13 11:50:21.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ======================================================================================================
2025-11-13 11:50:21.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Detector Report
2025-11-13 11:50:21.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ======================================================================================================
2025-11-13 11:50:21.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 	/Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm (depth 0)
2025-11-13 11:50:21.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 		NPM Package Lock: SUCCESS
2025-11-13 11:50:21.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 			Found file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/package-lock.json
2025-11-13 11:50:21.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 			Found file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/package.json
2025-11-13 11:50:21.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 11:50:21.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Detectors actions finished.
2025-11-13 11:50:21.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 11:50:21.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Project name: owasp-nodejs-goat
2025-11-13 11:50:21.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Project version: 1.3.0
2025-11-13 11:50:22.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 11:50:22.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Signature Scanner tool will not be run.
2025-11-13 11:50:22.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 11:50:22.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Vulnerability Impact Analysis tool will not be run.
2025-11-13 11:50:22.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 11:50:22.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- IaC Scanner tool will not be run.
2025-11-13 11:50:22.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 11:50:22.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ##################################################################################################
2025-11-13 11:50:22.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- #                                                                                                #
2025-11-13 11:50:22.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- #  Product Notice                                                                                #
2025-11-13 11:50:22.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- #  © 2024 Black Duck Software, Inc.                                                              #
2025-11-13 11:50:22.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- #  This Black Duck Component Locator and all associated documentation are proprietary            #
2025-11-13 11:50:22.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- #  to Black Duck Software, Inc. and may only be used pursuant to the terms and conditions of a   #
2025-11-13 11:50:22.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- #  written license agreement with Black Duck Software, Inc. All other use, reproduction,         #
2025-11-13 11:50:22.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- #  modification, or distribution of the Black Duck Component Locator or the associated           #
2025-11-13 11:50:22.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- #  documentation is strictly prohibited.                                                         #
2025-11-13 11:50:22.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- #                                                                                                #
2025-11-13 11:50:22.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ##################################################################################################
2025-11-13 11:50:22.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Running Component Locator v1.1.12 on /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm
2025-11-13 11:51:04.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Component Location Analysis file saved at: /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/detect/runs/2025-11-13-06-20-20-813/scan/components-with-locations.json
2025-11-13 11:51:04.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 11:51:04.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 11:51:04.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 11:51:04.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Creating status file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/detect/runs/2025-11-13-06-20-20-813/status/status.json
2025-11-13 11:51:04.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 11:51:04.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Skipping cleanup, it is disabled.
2025-11-13 11:51:04.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 11:51:04.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 11:51:04.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ======== Detect Result ========
2025-11-13 11:51:04.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 11:51:04.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Component Location Analysis File: /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/detect/runs/2025-11-13-06-20-20-813/scan/components-with-locations.json
2025-11-13 11:51:04.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 11:51:04.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ======== Detect Status ========
2025-11-13 11:51:04.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 11:51:04.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- NPM: SUCCESS
2025-11-13 11:51:04.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Overall Status: SUCCESS - Detect exited successfully.
2025-11-13 11:51:04.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 11:51:04.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ===============================
2025-11-13 11:51:04.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 11:51:04.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Detect duration: 00h 00m 44s 089ms
2025-11-13 11:51:04.3924 IST [Polaris SCA Package Manager Scan] INFO: Provided value for resource 'detect.completed'
2025-11-13 11:51:04.3926 IST [Polaris SCA Package Manager Scan] INFO: Provided value for resource 'polaris.test.sca.tests.scaPackage.artifacts.path'
2025-11-13 11:51:04.3927 IST [Polaris SCA Package Manager Scan] INFO: Adapter finished
2025-11-13 11:51:04.4293 IST [Polaris Artifacts Uploader] INFO: uploading artifact for "SAST(sastFull)" assessment with id "3a4f59f6-50e6-4638-8b92-61bcae8f14f1"
2025-11-13 11:51:04.4298 IST [Polaris Artifacts Uploader] INFO: uploading artifact for "SCA(scaPackage)" assessment with id "9fa16972-df2b-4ced-be31-811d3073c82e"
2025-11-13 11:51:05.3939 IST [Polaris Artifacts Uploader] INFO: Uploading artifact /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/idir.zip for "SAST(sastFull)" assessment
2025-11-13 11:51:05.4154 IST [Polaris Artifacts Uploader] INFO: Uploading artifact /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/blackduck-sca-artifacts.zip for "SCA(scaPackage)" assessment
2025-11-13 11:51:05.4369 IST [Polaris Artifacts Uploader] INFO: Uploading Progress of "SAST(sastFull)" artifact:   4%  16384/383983
2025-11-13 11:51:05.4458 IST [Polaris Artifacts Uploader] INFO: Uploading Progress of "SAST(sastFull)" artifact:  29%  114688/383983
2025-11-13 11:51:05.4581 IST [Polaris Artifacts Uploader] INFO: Uploading Progress of "SCA(scaPackage)" artifact:   7%  16384/208460
2025-11-13 11:51:05.4660 IST [Polaris Artifacts Uploader] INFO: Uploading Progress of "SAST(sastFull)" artifact:  55%  212992/383983
2025-11-13 11:51:05.4663 IST [Polaris Artifacts Uploader] INFO: Uploading Progress of "SCA(scaPackage)" artifact:  39%  81920/208460
2025-11-13 11:51:05.4737 IST [Polaris Artifacts Uploader] INFO: Uploading Progress of "SAST(sastFull)" artifact:  81%  311296/383983
2025-11-13 11:51:05.4738 IST [Polaris Artifacts Uploader] INFO: Uploading Progress of "SCA(scaPackage)" artifact:  70%  147456/208460
2025-11-13 11:51:05.4763 IST [Polaris Artifacts Uploader] INFO: Uploading Progress of "SAST(sastFull)" artifact: 100%  383983/383983
2025-11-13 11:51:05.4971 IST [Polaris Artifacts Uploader] INFO: Uploading Progress of "SCA(scaPackage)" artifact: 100%  208460/208460
2025-11-13 11:51:06.7222 IST [Polaris Artifacts Uploader] INFO: successfully uploaded artifact "/Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/blackduck-sca-artifacts.zip"
2025-11-13 11:51:07.0317 IST [Polaris Artifacts Uploader] INFO: successfully uploaded artifact "/Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/idir.zip"
2025-11-13 11:51:07.2540 IST [Polaris Artifacts Uploader] INFO: successfully resumed "SCA(scaPackage)" assessment with id "9fa16972-df2b-4ced-be31-811d3073c82e"
2025-11-13 11:51:07.5421 IST [Polaris Artifacts Uploader] INFO: successfully resumed "SAST(sastFull)" assessment with id "3a4f59f6-50e6-4638-8b92-61bcae8f14f1"
2025-11-13 11:51:07.5661 IST [Polaris Artifacts Uploader] INFO: Provided value for resource 'polaris.test.sast.tests.sastFull.artifacts.uploadSuccessful'
2025-11-13 11:51:07.5666 IST [Polaris Artifacts Uploader] INFO: Provided value for resource 'polaris.test.sca.tests.scaPackage.artifacts.uploadSuccessful'
2025-11-13 11:51:07.5671 IST [Polaris Artifacts Uploader] INFO: Adapter finished
2025-11-13 11:51:07.6374 IST [Polaris Waiter] INFO: Waiting for test with assessment type "SAST(sastFull)" and id "3a4f59f6-50e6-4638-8b92-61bcae8f14f1"
2025-11-13 11:51:07.6381 IST [Polaris Waiter] INFO: Waiting for test with assessment type "SCA(scaPackage)" and id "9fa16972-df2b-4ced-be31-811d3073c82e"
2025-11-13 11:51:08.0572 IST [Polaris Waiter] INFO: Polling Test Manager: state of test with assessment type "SCA(scaPackage)" and id "9fa16972-df2b-4ced-be31-811d3073c82e" is "Queuing"
2025-11-13 11:51:08.0574 IST [Polaris Waiter] INFO: Polling Test Manager: state of test with assessment type "SAST(sastFull)" and id "3a4f59f6-50e6-4638-8b92-61bcae8f14f1" is "Queuing"
2025-11-13 11:51:59.7676 IST [Polaris Waiter] INFO: Polling Test Manager: state of test with assessment type "SCA(scaPackage)" and id "9fa16972-df2b-4ced-be31-811d3073c82e" is "Scanning & Publishing"
2025-11-13 11:51:59.7677 IST [Polaris Waiter] INFO: Polling Test Manager: state of test with assessment type "SAST(sastFull)" and id "3a4f59f6-50e6-4638-8b92-61bcae8f14f1" is "Scanning"
2025-11-13 11:52:20.4118 IST [Polaris Waiter] INFO: Polling Test Manager: state of test with assessment type "SAST(sastFull)" and id "3a4f59f6-50e6-4638-8b92-61bcae8f14f1" is "In Progress"
2025-11-13 11:52:30.7058 IST [Polaris Waiter] INFO: test with assessment type "SCA(scaPackage)" and id "9fa16972-df2b-4ced-be31-811d3073c82e" completed successfully
2025-11-13 11:52:30.7290 IST [Polaris Waiter] INFO: test with assessment type "SAST(sastFull)" and id "3a4f59f6-50e6-4638-8b92-61bcae8f14f1" completed successfully
2025-11-13 11:52:30.7539 IST [Polaris Waiter] INFO: Provided value for resource 'polaris.test.sca.tests.scaPackage.completed'
2025-11-13 11:52:30.7554 IST [Polaris Waiter] INFO: Provided value for resource 'polaris.test.sast.tests.sastFull.completed'
2025-11-13 11:52:30.7604 IST [Polaris Waiter] INFO: Adapter finished
2025-11-13 11:52:30.8326 IST [Polaris Policy Checker] INFO: Checking for policy violations for "SAST(sastFull)" assessment...
2025-11-13 11:52:30.8332 IST [Polaris Policy Checker] INFO: Checking for policy violations for "SCA(scaPackage)" assessment...
2025-11-13 11:52:31.3077 IST [Polaris Policy Checker] INFO: no policies were violated to break the build
2025-11-13 11:52:31.3318 IST [Polaris Policy Checker] INFO: Adapter finished
2025-11-13 11:52:31.3726 IST [Polaris Issues Fetcher] INFO: Fetching issues for "SAST(sastFull)" assessment
2025-11-13 11:52:31.3734 IST [Polaris Issues Fetcher] INFO: Fetching issues for "SCA(scaPackage)" assessment
2025-11-13 11:52:31.7443 IST [Polaris Issues Fetcher] INFO: Successfully fetched issues for assessment type "SAST(sastFull)" with id "3a4f59f6-50e6-4638-8b92-61bcae8f14f1"
 {
 "critical": 0,
 "high": 2,
 "informational": 0,
 "low": 25,
 "medium": 13
}
2025-11-13 11:52:31.7575 IST [Polaris Issues Fetcher] INFO: Successfully fetched issues for assessment type "SCA(scaPackage)" with id "9fa16972-df2b-4ced-be31-811d3073c82e"
 {
 "critical": 6,
 "high": 109,
 "informational": 0,
 "low": 15,
 "medium": 133
}
2025-11-13 11:52:31.7870 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.SAST.tests.sastFull.issues.medium'
2025-11-13 11:52:31.7872 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.SAST.tests.sastFull.issues.critical'
2025-11-13 11:52:31.7874 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.SAST.tests.sastFull.issues.high'
2025-11-13 11:52:31.7876 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.SAST.tests.sastFull.issues.informational'
2025-11-13 11:52:31.7878 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.SAST.tests.sastFull.issues.low'
2025-11-13 11:52:31.7879 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.SCA.tests.scaPackage.issues.low'
2025-11-13 11:52:31.7881 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.SCA.tests.scaPackage.issues.critical'
2025-11-13 11:52:31.7883 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.SCA.tests.scaPackage.issues.high'
2025-11-13 11:52:31.7885 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.SCA.tests.scaPackage.issues.informational'
2025-11-13 11:52:31.7887 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.SCA.tests.scaPackage.issues.medium'
2025-11-13 11:52:31.7890 IST [Polaris Issues Fetcher] INFO: Adapter finished
2025-11-13 11:52:31.8430 IST [Polaris Status Provider] INFO: Results for test "SAST(sastFull)" with ID "3a4f59f6-50e6-4638-8b92-61bcae8f14f1" are available at https://poc.polaris.blackduck.com/portfolio/portfolios/edf596d3-b54f-4a6b-9e5c-209f2e526c67/portfolio-items/22dbe4fe-fa86-4760-a4ce-19e939247488/projects/024fe447-c19e-451d-9028-2b887efd3629/tests/3a4f59f6-50e6-4638-8b92-61bcae8f14f1/detected-issues
2025-11-13 11:52:31.8434 IST [Polaris Status Provider] INFO: Results for test "SCA(scaPackage)" with ID "9fa16972-df2b-4ced-be31-811d3073c82e" are available at https://poc.polaris.blackduck.com/portfolio/portfolios/edf596d3-b54f-4a6b-9e5c-209f2e526c67/portfolio-items/22dbe4fe-fa86-4760-a4ce-19e939247488/projects/024fe447-c19e-451d-9028-2b887efd3629/tests/9fa16972-df2b-4ced-be31-811d3073c82e/detected-issues
2025-11-13 11:52:31.8435 IST [Polaris Status Provider] INFO: Polaris issues view for project "sigma-rapid-scan", branch "main" is available at https://poc.polaris.blackduck.com/portfolio/portfolios/edf596d3-b54f-4a6b-9e5c-209f2e526c67/portfolio-items/22dbe4fe-fa86-4760-a4ce-19e939247488/projects/024fe447-c19e-451d-9028-2b887efd3629/issues?branchId=7b982e51-705a-48b2-acbd-95437cf2c8b3
2025-11-13 11:52:31.8521 IST [Polaris Status Provider] INFO: Provided value for resource 'polaris.test.SCA.tests.scaPackage.summary.url'
2025-11-13 11:52:31.8524 IST [Polaris Status Provider] INFO: Provided value for resource 'polaris.test.SAST.tests.sastFull.summary.url'
2025-11-13 11:52:31.8525 IST [Polaris Status Provider] INFO: Provided value for resource 'polaris.project.issues.url'
2025-11-13 11:52:31.8528 IST [Polaris Status Provider] INFO: Adapter finished
******************************* END EXECUTION OF BRIDGE CLI *******************************
[Security Scan] INFO: Retrieving the issue count from the scan results
[Security Scan] INFO: Total issues found: 303
[Security Scan] INFO: Security Scan execution is successful
**************************** END EXECUTION OF BLACK DUCK SECURITY SCAN ****************************
[Pipeline] }
[Pipeline] // dir
[Pipeline] }
[Pipeline] // script
[Pipeline] }
[Pipeline] // stage
[Pipeline] stage
[Pipeline] { (Declarative: Post Actions)
[Pipeline] echo
Black Duck Logs Publisher - Starting log upload process
[Pipeline] echo
Configuration: [githubOrg:polaris-jenkins-samples, repoName:sigma-rapid-scan, credentialsId:github-pat-logs-publisher, maxRetries:3, retentionCount:5, jobNamePrefixes:[MBP_Github_, MBP_, Github_, Pipeline_, Job_, Build_]]
[Pipeline] echo
Job Name: MBP_Github_Polaris_Rapid_Scan/main
[Pipeline] echo
Build Number: 4
[Pipeline] echo
GitHub Organization: polaris-jenkins-samples
[Pipeline] withCredentials
Masking supported pattern matches of $GITHUB_TOKEN
[Pipeline] {
[Pipeline] echo
Using configured repository name: sigma-rapid-scan
[Pipeline] echo
Target repository: polaris-jenkins-samples/sigma-rapid-scan
[Pipeline] echo
LogProcessor: captureJenkinsLogs called
```

---

*Log generated by Black Duck Logs Publisher*