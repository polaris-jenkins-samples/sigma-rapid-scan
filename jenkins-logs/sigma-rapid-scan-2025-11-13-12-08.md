# Jenkins Execution Log

## Build Information
- **Job Name:** `MBP_Github_Polaris_Rapid_Scan/main`
- **Build Number:** #5
- **Build Status:** 🟢 **SUCCESS**
- **Duration:** 4 min 44 sec and counting
- **Timestamp:** 2025-11-13 12:08:28 UTC

---

## Console Output

```
Started by user admin
Connecting to https://api.github.com using madhusud@blackduck.com/****** (Github_Username_PAT)
Obtained nodejs-npm/Jenkinsfile from ca7fb92ba6ca4193d343df28f8430bd7ce9583b1
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
Still waiting to schedule task
‘mac-sh’ is offline
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
Checking out Revision ca7fb92ba6ca4193d343df28f8430bd7ce9583b1 (main)
Commit message: "Jenkins log upload - Build #4"
 > git config core.sparsecheckout # timeout=10
 > git checkout -f ca7fb92ba6ca4193d343df28f8430bd7ce9583b1 # timeout=10
 > git rev-list --no-walk 2123a6e24e28f43ca417556841bf1498fc5d52e8 # timeout=10
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

up to date, audited 1412 packages in 21s

32 packages are looking for funding
  run `npm fund` for details

136 vulnerabilities (9 low, 35 moderate, 57 high, 35 critical)

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
[Security Scan] INFO:  --- polaris_test_sast_type = SAST_RAPID
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
[Security Scan] INFO: Executable command line arguments: /Users/madhusud/bridge-cli-bundle/bridge-cli-bundle-macos_arm/bridge-cli --stage polaris --input /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/polaris_input3093779938535483475.json --out .bridge/output/scan_info_out.json

******************************* START EXECUTION OF BRIDGE CLI *******************************
2025-11-13 12:06:46.5645 IST [Bridge CLI] INFO: Using cache directory: /Users/madhusud/bridge-cli-bundle/bridge-cli-bundle-macos_arm
2025-11-13 12:06:46.5759 IST [Bridge CLI] INFO: Found version "3.0.371" in registry for workflow "polaris", trying to load it from local cache
2025-11-13 12:06:47.9356 IST [Bridge CLI] INFO: Input Resources:
2025-11-13 12:06:47.9356 IST [Bridge CLI] INFO: resource = value [source]
2025-11-13 12:06:47.9357 IST [Bridge CLI] INFO: ------------------------------------------------------------
2025-11-13 12:06:47.9357 IST [Bridge CLI] INFO: network.airgap = false [polaris_input3093779938535483475.json]
2025-11-13 12:06:47.9357 IST [Bridge CLI] INFO: polaris.accesstoken = ***************************************** [polaris_input3093779938535483475.json]
2025-11-13 12:06:47.9357 IST [Bridge CLI] INFO: polaris.application.name = sigma-rapid-scan [polaris_input3093779938535483475.json]
2025-11-13 12:06:47.9357 IST [Bridge CLI] INFO: polaris.assessment.types = [SAST SCA] [polaris_input3093779938535483475.json]
2025-11-13 12:06:47.9357 IST [Bridge CLI] INFO: polaris.branch.name = main [polaris_input3093779938535483475.json]
2025-11-13 12:06:47.9357 IST [Bridge CLI] INFO: polaris.project.name = sigma-rapid-scan [polaris_input3093779938535483475.json]
2025-11-13 12:06:47.9357 IST [Bridge CLI] INFO: polaris.serverUrl = https://poc.polaris.blackduck.com [polaris_input3093779938535483475.json]
2025-11-13 12:06:47.9357 IST [Bridge CLI] INFO: polaris.test.sast.type = [SAST_RAPID] [polaris_input3093779938535483475.json]
2025-11-13 12:06:47.9358 IST [Bridge CLI] INFO: polaris.waitForScan = true [polaris_input3093779938535483475.json]
2025-11-13 12:06:47.9358 IST [Bridge CLI] INFO: ------------------------------------------------------------
2025-11-13 12:06:47.9358 IST [Bridge CLI] INFO: Starting adapters for stage polaris
2025-11-13 12:06:47.9380 IST [Bridge CLI] INFO: Starting Adapter: Polaris Controller
2025-11-13 12:06:47.9380 IST [Bridge CLI] INFO: Starting Adapter: Polaris Status Provider
2025-11-13 12:06:47.9380 IST [Bridge CLI] INFO: Starting Adapter: Polaris Initializer
2025-11-13 12:06:47.9380 IST [Bridge CLI] INFO: Starting Adapter: Polaris SCM Discovery
2025-11-13 12:06:48.0212 IST [Polaris SCM Discovery] INFO: Adapter finished
2025-11-13 12:06:48.0249 IST [Bridge CLI] INFO: Starting Adapter: Set Polaris Assessment Mode to CI
2025-11-13 12:06:48.0250 IST [Set Polaris Assessment Mode to CI] INFO: Provided value for resource 'polaris.assessment.mode'
2025-11-13 12:06:48.0251 IST [Set Polaris Assessment Mode to CI] INFO: Adapter finished
2025-11-13 12:06:48.0284 IST [Bridge CLI] INFO: Starting Adapter: Create Polaris Project & Branch By Default
2025-11-13 12:06:48.0292 IST [Create Polaris Project & Branch By Default] INFO: Provided value for resource 'polaris.onboarding'
2025-11-13 12:06:48.0292 IST [Create Polaris Project & Branch By Default] INFO: Adapter finished
2025-11-13 12:06:50.8616 IST [Polaris Initializer] INFO: Successfully created test for "SCA(scaPackage)" assessment. The short test ID is "DONJSTA"
2025-11-13 12:06:50.9213 IST [Polaris Initializer] INFO: Successfully created test for "SAST(sastRapid)" assessment. The short test ID is "V2HV50D"
2025-11-13 12:06:50.9470 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.test.SAST.tests.sastRapid.id'
2025-11-13 12:06:50.9474 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.test.SCA.tests.scaPackage.id'
2025-11-13 12:06:50.9477 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.test.SAST.tests.sastRapid.shortId'
2025-11-13 12:06:50.9481 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.test.SCA.tests.scaPackage.shortId'
2025-11-13 12:06:50.9484 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.test.SAST.tests.sastRapid.streamId'
2025-11-13 12:06:50.9487 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.project.id'
2025-11-13 12:06:50.9488 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.branch.id'
2025-11-13 12:06:50.9489 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.portfolioid'
2025-11-13 12:06:50.9490 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.tenant.id'
2025-11-13 12:06:50.9491 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.application.id'
2025-11-13 12:06:50.9495 IST [Polaris Initializer] INFO: Adapter finished
2025-11-13 12:06:50.9624 IST [Bridge CLI] INFO: Starting Adapter: Check pull request
2025-11-13 12:06:51.0107 IST [Check pull request] INFO: Provided value for resource 'environment.scan.pull'
2025-11-13 12:06:51.0110 IST [Check pull request] INFO: Adapter finished
2025-11-13 12:06:51.0582 IST [Polaris Controller] INFO: Running for "sca" assessment with scan type "scaPackage"
2025-11-13 12:06:51.0586 IST [Polaris Controller] INFO: fetching recommended "detect" tool info...
2025-11-13 12:06:51.8430 IST [Polaris Controller] INFO: checking "detect" tool installation inside bridge home directory: /Users/madhusud/.blackduck/bridge/tools/blackduck-detect/10.4.0
2025-11-13 12:06:51.8433 IST [Polaris Controller] INFO: Running command:/Library/Java/JavaVirtualMachines/jdk-21.jdk/Contents/Home/bin/java -version
2025-11-13 12:06:51.9318 IST [Polaris Controller] INFO: Checking tool version for "detect" in "/Users/madhusud/.blackduck/bridge/tools/blackduck-detect/10.4.0"
2025-11-13 12:06:51.9361 IST [Polaris Controller] INFO: Got tool version for "detect": 10.4.0
2025-11-13 12:06:52.2247 IST [Polaris Controller] INFO: "detect" tool is already installed...
2025-11-13 12:06:52.2249 IST [Polaris Controller] INFO: Running for "sast" assessment with scan type "sastRapid"
2025-11-13 12:06:52.2249 IST [Polaris Controller] INFO: fetching recommended "Sigma" tool info...
2025-11-13 12:06:52.5227 IST [Polaris Controller] INFO: checking "Sigma" tool installation inside bridge home directory: /Users/madhusud/.blackduck/bridge/tools/sigma/2025.10.0
2025-11-13 12:06:52.5228 IST [Polaris Controller] INFO: Checking tool version for "sigma" in "/Users/madhusud/.blackduck/bridge/tools/sigma/2025.10.0"
2025-11-13 12:06:52.5230 IST [Polaris Controller] INFO: Running command:/Users/madhusud/.blackduck/bridge/tools/sigma/2025.10.0/sigma --version
2025-11-13 12:06:52.6140 IST [Polaris Controller] INFO: Got tool version for "sigma": 2025.10.0
2025-11-13 12:06:52.8984 IST [Polaris Controller] INFO: "Sigma" tool is already installed...
2025-11-13 12:06:52.9325 IST [Polaris Controller] INFO: Provided value for resource 'sigma.id'
2025-11-13 12:06:52.9327 IST [Polaris Controller] INFO: Provided value for resource 'detect.id'
2025-11-13 12:06:52.9328 IST [Bridge CLI] INFO: Starting adapters for stage polaris-sca-package
2025-11-13 12:06:52.9328 IST [Bridge CLI] INFO: Starting adapters for stage polaris-sast-rapid
2025-11-13 12:06:52.9328 IST [Bridge CLI] INFO: Starting adapters for stage polaris-artifacts-uploader
2025-11-13 12:06:52.9328 IST [Bridge CLI] INFO: Starting adapters for stage polaris-post-processing
2025-11-13 12:06:52.9341 IST [Bridge CLI] INFO: Starting Adapter: Polaris SCA Package Manager Scan
2025-11-13 12:06:52.9341 IST [Bridge CLI] INFO: Starting Adapter: Polaris Rapid SAST
2025-11-13 12:06:52.9341 IST [Bridge CLI] INFO: Starting Adapter: Polaris Artifacts Uploader
2025-11-13 12:06:52.9341 IST [Bridge CLI] INFO: Starting Adapter: Polaris Waiter
2025-11-13 12:06:52.9342 IST [Bridge CLI] INFO: Starting Adapter: Polaris Issues Fetcher
2025-11-13 12:06:52.9342 IST [Bridge CLI] INFO: Starting Adapter: Polaris Policy Checker
2025-11-13 12:06:52.9344 IST [Polaris Controller] INFO: Adapter finished
2025-11-13 12:06:52.9579 IST [Bridge CLI] INFO: Starting Adapter: Default Adapter for execution path
2025-11-13 12:06:52.9582 IST [Default Adapter for execution path] INFO: Provided value for resource 'detect.execution.path'
2025-11-13 12:06:52.9584 IST [Default Adapter for execution path] INFO: Adapter finished
2025-11-13 12:06:52.9758 IST [Bridge CLI] INFO: Starting Adapter: Default Adapter for execution path
2025-11-13 12:06:52.9767 IST [Default Adapter for execution path] INFO: Provided value for resource 'sigma.execution.path'
2025-11-13 12:06:52.9768 IST [Default Adapter for execution path] INFO: Adapter finished
2025-11-13 12:06:53.0174 IST [Polaris SCA Package Manager Scan] INFO: Running command /Library/Java/JavaVirtualMachines/jdk-21.jdk/Contents/Home/bin/java -jar /Users/madhusud/.blackduck/bridge/tools/blackduck-detect/10.4.0/detect-10.4.0.jar --detect.cleanup=false --detect.bdio.file.name=scan --detect.bdio.output.path=/Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/detect/bdio/blackduck_artifact --detect.output.path=/Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/detect --detect.tools=DETECTOR --detect.component.location.analysis.enabled=true --blackduck.offline.mode=true --blackduck.offline.mode.force.bdio=true
2025-11-13 12:06:53.0000 IST [Polaris SCA Package Manager Scan][main] WARNING: --- Detect-Self-Updater:  Self-Update feature is disabled because of the following reasons:
2025-11-13 12:06:53.0000 IST [Polaris SCA Package Manager Scan][main] WARNING: --- Detect-Self-Updater:  Detect in offline mode is incompatible with the Self-Update feature.
2025-11-13 12:06:53.0000 IST [Polaris SCA Package Manager Scan][main] WARNING: --- Detect-Self-Updater:  Black Duck URL is required for the Self-Update feature.
2025-11-13 12:06:54.3276 IST [Polaris SCA Package Manager Scan] INFO: ______     _            _
2025-11-13 12:06:54.3277 IST [Polaris SCA Package Manager Scan] INFO: |  _  \   | |          | |
2025-11-13 12:06:54.3277 IST [Polaris SCA Package Manager Scan] INFO: | | | |___| |_ ___  ___| |_
2025-11-13 12:06:54.3277 IST [Polaris SCA Package Manager Scan] INFO: | | | / _ \ __/ _ \/ __| __|
2025-11-13 12:06:54.3277 IST [Polaris SCA Package Manager Scan] INFO: | |/ /  __/ ||  __/ (__| |_
2025-11-13 12:06:54.3277 IST [Polaris SCA Package Manager Scan] INFO: |___/ \___|\__\___|\___|\__|
2025-11-13 12:06:54.3278 IST [Polaris SCA Package Manager Scan] INFO: 
2025-11-13 12:06:54.4491 IST [Polaris SCA Package Manager Scan] INFO: 
2025-11-13 12:06:54.4491 IST [Polaris SCA Package Manager Scan] INFO: Detect Version: 10.4.0
2025-11-13 12:06:54.4492 IST [Polaris SCA Package Manager Scan] INFO: 
2025-11-13 12:06:54.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 12:06:54.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Current property values:
2025-11-13 12:06:54.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- --property = value [notes]
2025-11-13 12:06:54.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ------------------------------------------------------------
2025-11-13 12:06:54.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- blackduck.offline.mode = true [cmd] 
2025-11-13 12:06:54.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- blackduck.offline.mode.force.bdio = true [cmd] 
2025-11-13 12:06:54.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- detect.bdio.file.name = scan [cmd] 
2025-11-13 12:06:54.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- detect.bdio.output.path = /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/detect/bdio/blackduck_artifact [cmd] 
2025-11-13 12:06:54.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- detect.cleanup = false [cmd] 
2025-11-13 12:06:54.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- detect.component.location.analysis.enabled = true [cmd] 
2025-11-13 12:06:54.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- detect.excluded.directories = /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge [env] 
2025-11-13 12:06:54.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- detect.output.path = /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/detect [cmd] 
2025-11-13 12:06:54.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- detect.tools = DETECTOR [cmd] 
2025-11-13 12:06:54.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ------------------------------------------------------------
2025-11-13 12:06:54.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 12:06:54.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Detect build date: 2025-04-24
2025-11-13 12:06:54.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Source directory: /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm
2025-11-13 12:06:54.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Output directory: /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/detect
2025-11-13 12:06:54.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Run directory: /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/detect/runs/2025-11-13-06-36-54-413
2025-11-13 12:06:54.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 12:06:54.0000 IST [Polaris SCA Package Manager Scan][main] WARNING: --- Correlated Scanning is not available for Rapid/Stateless scan mode or offline scanning. A correlation ID will not be set.
2025-11-13 12:06:54.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 12:06:54.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Docker tool will not be run.
2025-11-13 12:06:54.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 12:06:54.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Bazel tool will not be run.
2025-11-13 12:06:54.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 12:06:54.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Will include the Detectors tool.
2025-11-13 12:06:54.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Searching for detectors.
2025-11-13 12:06:54.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Evaluating detectors. This may take a while.
2025-11-13 12:06:55.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ======================================================================================================
2025-11-13 12:06:55.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Detector Report
2025-11-13 12:06:55.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ======================================================================================================
2025-11-13 12:06:55.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 	/Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm (depth 0)
2025-11-13 12:06:55.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 		NPM Package Lock: SUCCESS
2025-11-13 12:06:55.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 			Found file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/package-lock.json
2025-11-13 12:06:55.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 			Found file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/package.json
2025-11-13 12:06:55.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 12:06:55.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Detectors actions finished.
2025-11-13 12:06:55.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 12:06:55.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Project name: owasp-nodejs-goat
2025-11-13 12:06:55.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Project version: 1.3.0
2025-11-13 12:06:56.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 12:06:56.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Signature Scanner tool will not be run.
2025-11-13 12:06:56.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 12:06:56.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Vulnerability Impact Analysis tool will not be run.
2025-11-13 12:06:56.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 12:06:56.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- IaC Scanner tool will not be run.
2025-11-13 12:06:56.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 12:06:56.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ##################################################################################################
2025-11-13 12:06:56.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- #                                                                                                #
2025-11-13 12:06:56.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- #  Product Notice                                                                                #
2025-11-13 12:06:56.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- #  © 2024 Black Duck Software, Inc.                                                              #
2025-11-13 12:06:56.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- #  This Black Duck Component Locator and all associated documentation are proprietary            #
2025-11-13 12:06:56.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- #  to Black Duck Software, Inc. and may only be used pursuant to the terms and conditions of a   #
2025-11-13 12:06:56.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- #  written license agreement with Black Duck Software, Inc. All other use, reproduction,         #
2025-11-13 12:06:56.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- #  modification, or distribution of the Black Duck Component Locator or the associated           #
2025-11-13 12:06:56.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- #  documentation is strictly prohibited.                                                         #
2025-11-13 12:06:56.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- #                                                                                                #
2025-11-13 12:06:56.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ##################################################################################################
2025-11-13 12:06:56.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Running Component Locator v1.1.12 on /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm
2025-11-13 12:07:46.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Component Location Analysis file saved at: /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/detect/runs/2025-11-13-06-36-54-413/scan/components-with-locations.json
2025-11-13 12:07:46.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 12:07:46.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 12:07:46.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 12:07:46.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Creating status file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/detect/runs/2025-11-13-06-36-54-413/status/status.json
2025-11-13 12:07:46.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 12:07:46.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Skipping cleanup, it is disabled.
2025-11-13 12:07:46.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 12:07:46.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 12:07:46.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ======== Detect Result ========
2025-11-13 12:07:46.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 12:07:46.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Component Location Analysis File: /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/detect/runs/2025-11-13-06-36-54-413/scan/components-with-locations.json
2025-11-13 12:07:46.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 12:07:46.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ======== Detect Status ========
2025-11-13 12:07:46.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 12:07:46.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- NPM: SUCCESS
2025-11-13 12:07:46.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Overall Status: SUCCESS - Detect exited successfully.
2025-11-13 12:07:46.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 12:07:46.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ===============================
2025-11-13 12:07:46.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 12:07:46.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Detect duration: 00h 00m 53s 496ms
2025-11-13 12:07:46.8810 IST [Polaris SCA Package Manager Scan] INFO: Provided value for resource 'detect.completed'
2025-11-13 12:07:46.8812 IST [Polaris SCA Package Manager Scan] INFO: Provided value for resource 'polaris.test.sca.tests.scaPackage.artifacts.path'
2025-11-13 12:07:46.8815 IST [Polaris SCA Package Manager Scan] INFO: Adapter finished
2025-11-13 12:07:47.3013 IST [Polaris Rapid SAST] INFO: command: /Users/madhusud/.blackduck/bridge/tools/sigma/2025.10.0/sigma --disable-telemetry --internal-enable-telemetry --internal-dump-telemetry-to-file /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_rapid_sast/telemetry.json --internal-polaris-scan-log /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_rapid_sast/scanlog.json --internal-root-coverity-config analyze --internal-polaris-metrics-file /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_rapid_sast/metrics.json --internal-disable-checks-by-lang-in-coverity-v0 true --internal-polaris-scan-output /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_rapid_sast/scan --format AVRO-COMMIT
2025-11-13 12:07:47.3830 IST [Polaris Rapid SAST] INFO: Copyright (c) 2025 Black Duck Software, Inc.
2025-11-13 12:07:47.3831 IST [Polaris Rapid SAST] INFO: Sigma version : 2025.10.0
2025-11-13 12:07:47.3831 IST [Polaris Rapid SAST] INFO: For documentation and support, visit https://documentation.blackduck.com/bundle/sigma-ug/page/topics/sigma_user_guide.html
2025-11-13 12:07:47.3831 IST [Polaris Rapid SAST] INFO: By using this software, the user accepts the terms of Black Duck Software's end user software license and maintenance agreement found at: https://www.blackduck.com/company/legal.html
2025-11-13 12:07:47.3831 IST [Polaris Rapid SAST] INFO: 
2025-11-13 12:07:47.5492 IST [Polaris Rapid SAST] INFO: WARNING: No input was provided, analyzing current working directory
2025-11-13 12:07:48.9127 IST [Polaris Rapid SAST] INFO: [2025-11-13 06:37:48 (ThreadId(013)|RayonId(None))] Excluded 27874 file paths from analysis.
2025-11-13 12:07:48.0000 IST [Polaris Rapid SAST] INFO: Telemetry data conforms to schema e64f13671933fe956d8d8d73fa1d2a2308642cb2c67680b84fd4d1910a106893
2025-11-13 12:07:48.0000 IST [Polaris Rapid SAST] INFO: Analysis done in 1 second
2025-11-13 12:07:48.0000 IST [Polaris Rapid SAST] INFO: Found 43 defects
2025-11-13 12:07:48.9801 IST [Polaris Rapid SAST] INFO: 
2025-11-13 12:07:48.9801 IST [Polaris Rapid SAST] INFO: Identified
2025-11-13 12:07:48.9802 IST [Polaris Rapid SAST] INFO: 
2025-11-13 12:07:48.9802 IST [Polaris Rapid SAST] INFO: │File Type │Occurrences│
2025-11-13 12:07:48.9802 IST [Polaris Rapid SAST] INFO: ├──────────┼───────────┤
2025-11-13 12:07:48.9802 IST [Polaris Rapid SAST] INFO: │JavaScript│         44│
2025-11-13 12:07:48.9803 IST [Polaris Rapid SAST] INFO: │HTML      │         24│
2025-11-13 12:07:48.9803 IST [Polaris Rapid SAST] INFO: │JSON      │          8│
2025-11-13 12:07:48.9804 IST [Polaris Rapid SAST] INFO: │Unknown   │          8│
2025-11-13 12:07:48.9804 IST [Polaris Rapid SAST] INFO: │Markdown  │          3│
2025-11-13 12:07:48.9804 IST [Polaris Rapid SAST] INFO: │Dockerfile│          1│
2025-11-13 12:07:48.9804 IST [Polaris Rapid SAST] INFO: │YAML      │          1│
2025-11-13 12:07:48.9805 IST [Polaris Rapid SAST] INFO: 
2025-11-13 12:07:48.9805 IST [Polaris Rapid SAST] INFO: 
2025-11-13 12:07:48.9805 IST [Polaris Rapid SAST] INFO: Issues
2025-11-13 12:07:48.9805 IST [Polaris Rapid SAST] INFO: 
2025-11-13 12:07:48.9805 IST [Polaris Rapid SAST] INFO: │                        Type                         │                    Tags                     │Occurrences│
2025-11-13 12:07:48.9806 IST [Polaris Rapid SAST] INFO: ├─────────────────────────────────────────────────────┼─────────────────────────────────────────────┼───────────┤
2025-11-13 12:07:48.9806 IST [Polaris Rapid SAST] INFO: │hardcoded_secret_pattern                             │secret                                       │         10│
2025-11-13 12:07:48.9806 IST [Polaris Rapid SAST] INFO: │missing_iframe_sandbox_html                          │web, iframe                                  │          9│
2025-11-13 12:07:48.9806 IST [Polaris Rapid SAST] INFO: │reverse_tabnabbing_html                              │web, client, phishing                        │          4│
2025-11-13 12:07:48.9807 IST [Polaris Rapid SAST] INFO: │unsafe_eval_core_javascript                          │node, xss, rce                               │          3│
2025-11-13 12:07:48.9807 IST [Polaris Rapid SAST] INFO: │container_filesystem_write_docker_compose            │docker, iac, cis_benchmark, filesystem, authz│          2│
2025-11-13 12:07:48.9807 IST [Polaris Rapid SAST] INFO: │container_privilege_escalation_allowed_docker_compose│docker, iac, cis_benchmark, authz            │          2│
2025-11-13 12:07:48.9807 IST [Polaris Rapid SAST] INFO: │container_requesting_net_raw_docker_compose          │iac, docker, authz, network                  │          2│
2025-11-13 12:07:48.9808 IST [Polaris Rapid SAST] INFO: │least_privilege_violation_docker_compose             │iac, docker, authz                           │          2│
2025-11-13 12:07:48.9808 IST [Polaris Rapid SAST] INFO: │exposed_secret_ssh_keys                              │ssh, secret, keychain                        │          1│
2025-11-13 12:07:48.9808 IST [Polaris Rapid SAST] INFO: │expression_escaping_disabled_swig                    │swig, web, node, input_validation, xss       │          1│
2025-11-13 12:07:48.9809 IST [Polaris Rapid SAST] INFO: │missing_samesite_attribute_session_cookie_express    │web, express, node, session, cookie, csrf    │          1│
2025-11-13 12:07:48.9809 IST [Polaris Rapid SAST] INFO: │missing_secure_attribute_session_cookie_express      │web, cookie, express, info_leak, session     │          1│
2025-11-13 12:07:48.9809 IST [Polaris Rapid SAST] INFO: │missing_tls_node_http_server                         │web, node, missing_tls, info_leak, crypto    │          1│
2025-11-13 12:07:48.9809 IST [Polaris Rapid SAST] INFO: │open_redirect_core_javascript                        │dataflow, authz, input_validation            │          1│
2025-11-13 12:07:48.9809 IST [Polaris Rapid SAST] INFO: │root_path_attribute_cookie_express                   │web, cookie, express, info_leak, session     │          1│
2025-11-13 12:07:48.9809 IST [Polaris Rapid SAST] INFO: │unsafe_session_storage_express_session               │web, express, dos, session                   │          1│
2025-11-13 12:07:48.9810 IST [Polaris Rapid SAST] INFO: │verbose_server_banner_express                        │web, info_leak, express                      │          1│
2025-11-13 12:07:48.9810 IST [Polaris Rapid SAST] INFO: 
2025-11-13 12:07:48.9810 IST [Polaris Rapid SAST] INFO: Full results: /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_rapid_sast/scan
2025-11-13 12:07:48.9810 IST [Polaris Rapid SAST] INFO: 
2025-11-13 12:07:48.9810 IST [Polaris Rapid SAST] INFO: Found 43 issues in 1 second
2025-11-13 12:07:49.0110 IST [Polaris Rapid SAST] INFO: Provided value for resource 'sigma.completed'
2025-11-13 12:07:49.0112 IST [Polaris Rapid SAST] INFO: Provided value for resource 'sigma.output.directory'
2025-11-13 12:07:49.0113 IST [Polaris Rapid SAST] INFO: Provided value for resource 'sigma.output.logs'
2025-11-13 12:07:49.0114 IST [Polaris Rapid SAST] INFO: Provided value for resource 'sigma.output.metrics'
2025-11-13 12:07:49.0115 IST [Polaris Rapid SAST] INFO: Provided value for resource 'sigma.output.telemetry'
2025-11-13 12:07:49.0120 IST [Polaris Rapid SAST] INFO: Provided value for resource 'snippetGenerator.avro.dir'
2025-11-13 12:07:49.0121 IST [Polaris Rapid SAST] INFO: Provided value for resource 'polaris.test.sast.tests.sastRapid.artifacts.path'
2025-11-13 12:07:49.0124 IST [Polaris Rapid SAST] INFO: Adapter finished
2025-11-13 12:07:49.0763 IST [Polaris Artifacts Uploader] INFO: uploading artifact for "SAST(sastRapid)" assessment with id "3472e42b-9bdd-40ff-a38a-68b7e4b48e49"
2025-11-13 12:07:49.0767 IST [Polaris Artifacts Uploader] INFO: uploading artifact for "SCA(scaPackage)" assessment with id "d260128e-8a24-4da3-8a8a-e283f742b75f"
2025-11-13 12:07:50.4036 IST [Polaris Artifacts Uploader] INFO: Uploading artifact /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_rapid_sast/AVRO_SCAN_OUTPUT-SAST-3472e42b-9bdd-40ff-a38a-68b7e4b48e49-2025-11-13T12%3A07%3A48Z.zip for "SAST(sastRapid)" assessment
2025-11-13 12:07:50.4042 IST [Polaris Artifacts Uploader] INFO: Uploading artifact /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/blackduck-sca-artifacts.zip for "SCA(scaPackage)" assessment
2025-11-13 12:07:51.0628 IST [Polaris Artifacts Uploader] INFO: Uploading Progress of "SAST(sastRapid)" artifact:   3%  16384/455844
2025-11-13 12:07:51.0730 IST [Polaris Artifacts Uploader] INFO: Uploading Progress of "SCA(scaPackage)" artifact:   7%  16384/208944
2025-11-13 12:07:51.2795 IST [Polaris Artifacts Uploader] INFO: Uploading Progress of "SCA(scaPackage)" artifact:  39%  81920/208944
2025-11-13 12:07:51.2796 IST [Polaris Artifacts Uploader] INFO: Uploading Progress of "SAST(sastRapid)" artifact:  28%  131072/455844
2025-11-13 12:07:51.2806 IST [Polaris Artifacts Uploader] INFO: Uploading Progress of "SCA(scaPackage)" artifact:  70%  147456/208944
2025-11-13 12:07:51.7033 IST [Polaris Artifacts Uploader] INFO: Uploading Progress of "SCA(scaPackage)" artifact: 100%  208944/208944
2025-11-13 12:07:51.7042 IST [Polaris Artifacts Uploader] INFO: Uploading Progress of "SAST(sastRapid)" artifact:  53%  245760/455844
2025-11-13 12:07:51.9089 IST [Polaris Artifacts Uploader] INFO: Uploading Progress of "SAST(sastRapid)" artifact:  79%  360448/455844
2025-11-13 12:07:51.9273 IST [Polaris Artifacts Uploader] INFO: Uploading Progress of "SAST(sastRapid)" artifact: 100%  455844/455844
2025-11-13 12:07:52.1936 IST [Polaris Artifacts Uploader] INFO: successfully uploaded artifact "/Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/blackduck-sca-artifacts.zip"
2025-11-13 12:07:52.5944 IST [Polaris Artifacts Uploader] INFO: successfully uploaded artifact "/Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Rapid_Scan_main/nodejs-npm/.bridge/polaris_rapid_sast/AVRO_SCAN_OUTPUT-SAST-3472e42b-9bdd-40ff-a38a-68b7e4b48e49-2025-11-13T12%3A07%3A48Z.zip"
2025-11-13 12:07:52.7403 IST [Polaris Artifacts Uploader] INFO: successfully resumed "SCA(scaPackage)" assessment with id "d260128e-8a24-4da3-8a8a-e283f742b75f"
2025-11-13 12:07:53.0813 IST [Polaris Artifacts Uploader] INFO: successfully resumed "SAST(sastRapid)" assessment with id "3472e42b-9bdd-40ff-a38a-68b7e4b48e49"
2025-11-13 12:07:53.0893 IST [Polaris Artifacts Uploader] INFO: Provided value for resource 'polaris.test.sast.tests.sastRapid.artifacts.uploadSuccessful'
2025-11-13 12:07:53.0894 IST [Polaris Artifacts Uploader] INFO: Provided value for resource 'polaris.test.sca.tests.scaPackage.artifacts.uploadSuccessful'
2025-11-13 12:07:53.0897 IST [Polaris Artifacts Uploader] INFO: Adapter finished
2025-11-13 12:07:53.1506 IST [Polaris Waiter] INFO: Waiting for test with assessment type "SCA(scaPackage)" and id "d260128e-8a24-4da3-8a8a-e283f742b75f"
2025-11-13 12:07:53.1511 IST [Polaris Waiter] INFO: Waiting for test with assessment type "SAST(sastRapid)" and id "3472e42b-9bdd-40ff-a38a-68b7e4b48e49"
2025-11-13 12:07:53.9102 IST [Polaris Waiter] INFO: Polling Test Manager: state of test with assessment type "SAST(sastRapid)" and id "3472e42b-9bdd-40ff-a38a-68b7e4b48e49" is "Scanning"
2025-11-13 12:07:53.9152 IST [Polaris Waiter] INFO: Polling Test Manager: state of test with assessment type "SCA(scaPackage)" and id "d260128e-8a24-4da3-8a8a-e283f742b75f" is "Queuing"
2025-11-13 12:08:04.2266 IST [Polaris Waiter] INFO: test with assessment type "SAST(sastRapid)" and id "3472e42b-9bdd-40ff-a38a-68b7e4b48e49" completed successfully
2025-11-13 12:08:04.2364 IST [Polaris Waiter] INFO: Polling Test Manager: state of test with assessment type "SCA(scaPackage)" and id "d260128e-8a24-4da3-8a8a-e283f742b75f" is "Scanning & Publishing"
2025-11-13 12:08:24.8825 IST [Polaris Waiter] INFO: test with assessment type "SCA(scaPackage)" and id "d260128e-8a24-4da3-8a8a-e283f742b75f" completed successfully
2025-11-13 12:08:24.8895 IST [Polaris Waiter] INFO: Provided value for resource 'polaris.test.sast.tests.sastRapid.completed'
2025-11-13 12:08:24.8896 IST [Polaris Waiter] INFO: Provided value for resource 'polaris.test.sca.tests.scaPackage.completed'
2025-11-13 12:08:24.8899 IST [Polaris Waiter] INFO: Adapter finished
2025-11-13 12:08:24.9599 IST [Polaris Issues Fetcher] INFO: Fetching issues for "SAST(sastRapid)" assessment
2025-11-13 12:08:24.9605 IST [Polaris Issues Fetcher] INFO: Fetching issues for "SCA(scaPackage)" assessment
2025-11-13 12:08:25.9736 IST [Polaris Issues Fetcher] INFO: Successfully fetched issues for assessment type "SCA(scaPackage)" with id "d260128e-8a24-4da3-8a8a-e283f742b75f"
 {
 "critical": 6,
 "high": 109,
 "informational": 0,
 "low": 15,
 "medium": 133
}
2025-11-13 12:08:25.9900 IST [Polaris Issues Fetcher] INFO: Successfully fetched issues for assessment type "SAST(sastRapid)" with id "3472e42b-9bdd-40ff-a38a-68b7e4b48e49"
 {
 "critical": 0,
 "high": 2,
 "informational": 0,
 "low": 25,
 "medium": 12
}
2025-11-13 12:08:25.9975 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.sast.tests.sastRapid.issues.low'
2025-11-13 12:08:25.9977 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.sast.tests.sastRapid.issues.medium'
2025-11-13 12:08:25.9979 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.sast.tests.sastRapid.issues.critical'
2025-11-13 12:08:25.9982 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.sast.tests.sastRapid.issues.informational'
2025-11-13 12:08:25.9986 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.sast.tests.sastRapid.issues.high'
2025-11-13 12:08:25.9987 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.SCA.tests.scaPackage.issues.medium'
2025-11-13 12:08:25.9989 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.SCA.tests.scaPackage.issues.critical'
2025-11-13 12:08:25.9990 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.SCA.tests.scaPackage.issues.high'
2025-11-13 12:08:25.9992 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.SCA.tests.scaPackage.issues.low'
2025-11-13 12:08:25.9993 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.SCA.tests.scaPackage.issues.informational'
2025-11-13 12:08:25.9996 IST [Polaris Issues Fetcher] INFO: Adapter finished
2025-11-13 12:08:26.0391 IST [Polaris Policy Checker] INFO: Checking for policy violations for "SCA(scaPackage)" assessment...
2025-11-13 12:08:26.0400 IST [Polaris Policy Checker] INFO: Checking for policy violations for "SAST(sastRapid)" assessment...
2025-11-13 12:08:26.9701 IST [Polaris Policy Checker] INFO: no policies were violated to break the build
2025-11-13 12:08:26.9768 IST [Polaris Policy Checker] INFO: Adapter finished
2025-11-13 12:08:27.0314 IST [Polaris Status Provider] INFO: Results for test "SCA(scaPackage)" with ID "d260128e-8a24-4da3-8a8a-e283f742b75f" are available at https://poc.polaris.blackduck.com/portfolio/portfolios/edf596d3-b54f-4a6b-9e5c-209f2e526c67/portfolio-items/22dbe4fe-fa86-4760-a4ce-19e939247488/projects/024fe447-c19e-451d-9028-2b887efd3629/tests/d260128e-8a24-4da3-8a8a-e283f742b75f/detected-issues
2025-11-13 12:08:27.0317 IST [Polaris Status Provider] INFO: Results for test "SAST(sastRapid)" with ID "3472e42b-9bdd-40ff-a38a-68b7e4b48e49" are available at https://poc.polaris.blackduck.com/portfolio/portfolios/edf596d3-b54f-4a6b-9e5c-209f2e526c67/portfolio-items/22dbe4fe-fa86-4760-a4ce-19e939247488/projects/024fe447-c19e-451d-9028-2b887efd3629/tests/3472e42b-9bdd-40ff-a38a-68b7e4b48e49/detected-issues
2025-11-13 12:08:27.0317 IST [Polaris Status Provider] INFO: Polaris issues view for project "sigma-rapid-scan", branch "main" is available at https://poc.polaris.blackduck.com/portfolio/portfolios/edf596d3-b54f-4a6b-9e5c-209f2e526c67/portfolio-items/22dbe4fe-fa86-4760-a4ce-19e939247488/projects/024fe447-c19e-451d-9028-2b887efd3629/issues?branchId=7b982e51-705a-48b2-acbd-95437cf2c8b3
2025-11-13 12:08:27.0383 IST [Polaris Status Provider] INFO: Provided value for resource 'polaris.test.SAST.tests.sastRapid.summary.url'
2025-11-13 12:08:27.0384 IST [Polaris Status Provider] INFO: Provided value for resource 'polaris.test.SCA.tests.scaPackage.summary.url'
2025-11-13 12:08:27.0385 IST [Polaris Status Provider] INFO: Provided value for resource 'polaris.project.issues.url'
2025-11-13 12:08:27.0387 IST [Polaris Status Provider] INFO: Adapter finished
******************************* END EXECUTION OF BRIDGE CLI *******************************
[Security Scan] INFO: Retrieving the issue count from the scan results
[Security Scan] INFO: Total issues found: 263
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
Build Number: 5
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