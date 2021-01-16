---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/new-AzImageBuilderCustomizerObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
ms.openlocfilehash: 3e67452a5d5e11fa4aa96d1b38b80a4284c21f00
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279043"
---
# <span data-ttu-id="5f5fe-101">New-AzImageBuilderCustomizerObject</span><span class="sxs-lookup"><span data-stu-id="5f5fe-101">New-AzImageBuilderCustomizerObject</span></span>

## <span data-ttu-id="5f5fe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5f5fe-102">SYNOPSIS</span></span>
<span data-ttu-id="5f5fe-103">描述影像自訂單位</span><span class="sxs-lookup"><span data-stu-id="5f5fe-103">Describes a unit of image customization</span></span>

## <span data-ttu-id="5f5fe-104">句法</span><span class="sxs-lookup"><span data-stu-id="5f5fe-104">SYNTAX</span></span>

### <span data-ttu-id="5f5fe-105">ShellCustomizer (預設) </span><span class="sxs-lookup"><span data-stu-id="5f5fe-105">ShellCustomizer (Default)</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -ShellCustomizer [-Inline <String[]>]
 [-ScriptUri <String>] [-Sha256Checksum <String>] [<CommonParameters>]
```

### <span data-ttu-id="5f5fe-106">FileCustomizer</span><span class="sxs-lookup"><span data-stu-id="5f5fe-106">FileCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -FileCustomizer [-Destination <String>]
 [-Sha256Checksum <String>] [-SourceUri <String>] [<CommonParameters>]
```

### <span data-ttu-id="5f5fe-107">PowerShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="5f5fe-107">PowerShellCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -PowerShellCustomizer [-Inline <String[]>]
 [-RunElevated <Boolean>] [-ScriptUri <String>] [-Sha256Checksum <String>] [-ValidExitCode <Int32[]>]
 [<CommonParameters>]
```

### <span data-ttu-id="5f5fe-108">RestartCustomizer</span><span class="sxs-lookup"><span data-stu-id="5f5fe-108">RestartCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -RestartCustomizer [-RestartCheckCommand <String>]
 [-RestartCommand <String>] [-RestartTimeout <String>] [<CommonParameters>]
```

### <span data-ttu-id="5f5fe-109">WindowsUpdateCustomizer</span><span class="sxs-lookup"><span data-stu-id="5f5fe-109">WindowsUpdateCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -WindowsUpdateCustomizer [-Filter <String[]>]
 [-SearchCriterion <String>] [-UpdateLimit <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="5f5fe-110">說明</span><span class="sxs-lookup"><span data-stu-id="5f5fe-110">DESCRIPTION</span></span>
<span data-ttu-id="5f5fe-111">描述影像自訂單位</span><span class="sxs-lookup"><span data-stu-id="5f5fe-111">Describes a unit of image customization</span></span>

## <span data-ttu-id="5f5fe-112">示例</span><span class="sxs-lookup"><span data-stu-id="5f5fe-112">EXAMPLES</span></span>

### <span data-ttu-id="5f5fe-113">範例1：建立 windows 更新定制器</span><span class="sxs-lookup"><span data-stu-id="5f5fe-113">Example 1: Create a windows update customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -WindowsUpdateCustomizer -Filter ("BrowseOnly", "IsInstalled") -SearchCriterion "BrowseOnly=0 and IsInstalled=0"  -UpdateLimit 100 -CustomizerName 'WindUpdate'

Name       Type          Filter                    SearchCriterion                UpdateLimit
----       ----          ------                    ---------------                -----------
WindUpdate WindowsUpdate {BrowseOnly, IsInstalled} BrowseOnly=0 and IsInstalled=0 100
```

<span data-ttu-id="5f5fe-114">這個命令會建立 windows 更新定制器。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-114">This command creates a windows update customizer.</span></span>

### <span data-ttu-id="5f5fe-115">範例2：建立檔案定制器</span><span class="sxs-lookup"><span data-stu-id="5f5fe-115">Example 2: Create a file customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -FileCustomizer -CustomizerName 'filecus' -Destination 'c:\\buildArtifacts\\index.html' -SourceUri 'https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/index.html'

Name    Type Destination                    Sha256Checksum SourceUri
----    ---- -----------                    -------------- ---------
filecus File c:\\buildArtifacts\\index.html                https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/…

```

<span data-ttu-id="5f5fe-116">這個命令會建立檔案定制器。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-116">This command creates a file customizer.</span></span>

### <span data-ttu-id="5f5fe-117">範例3：建立 powershell 定制器</span><span class="sxs-lookup"><span data-stu-id="5f5fe-117">Example 3: Create a powershell customizer</span></span>
```powershell
PS C:\> $inline = @("mkdir c:\\buildActions", "echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt")
PS C:\> New-AzImageBuilderCustomizerObject -PowerShellCustomizer -CustomizerName settingUpMgmtAgtPath -RunElevated $false -Inline $inline

Name                 Type       Inline                                                                                                  RunElevated ScriptUri Sha256Checksum
----                 ----       ------                                                                                                  ----------- --------- --------------
settingUpMgmtAgtPath PowerShell {mkdir c:\\buildActions, echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt} False

```

<span data-ttu-id="5f5fe-118">這個命令會建立 powershell 定制器。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-118">This command creates a powershell customizer.</span></span>

### <span data-ttu-id="5f5fe-119">範例4：建立重新開機定制器</span><span class="sxs-lookup"><span data-stu-id="5f5fe-119">Example 4: Create a restart customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -RestartCustomizer -CustomizerName 'restcus' -RestartCommand 'shutdown /f /r /t 0 /c \"packer restart\"' -RestartCheckCommand 'powershell -command "& {Write-Output "restarted."}"' -RestartTimeout '10m'

Name    Type           RestartCheckCommand                                 RestartCommand                            RestartTimeout
----    ----           -------------------                                 --------------                            --------------
restcus WindowsRestart powershell -command "& {Write-Output "restarted."}" shutdown /f /r /t 0 /c \"packer restart\" 10m
```

<span data-ttu-id="5f5fe-120">這個命令會建立重新開機定制器。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-120">This command creates a restart customizer.</span></span>

### <span data-ttu-id="5f5fe-121">範例5：建立 [殼定制器]</span><span class="sxs-lookup"><span data-stu-id="5f5fe-121">Example 5: Create a shell customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -ShellCustomizer -CustomizerName downloadBuildArtifacts -ScriptUri "https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh" 

Name                   Type  Inline ScriptUri                                                                                                      Sha256Checksum
----                   ----  ------ ---------                                                                                                      --------------
downloadBuildArtifacts Shell        https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh
```

<span data-ttu-id="5f5fe-122">這個命令會建立一個 shell 定制器。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-122">This command creates a shell customizer.</span></span>

## <span data-ttu-id="5f5fe-123">參數</span><span class="sxs-lookup"><span data-stu-id="5f5fe-123">PARAMETERS</span></span>

### <span data-ttu-id="5f5fe-124">-CustomizerName</span><span class="sxs-lookup"><span data-stu-id="5f5fe-124">-CustomizerName</span></span>
<span data-ttu-id="5f5fe-125">好記的名稱，以提供此自訂步驟的內容的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-125">Friendly Name to provide context on what this customization step does.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f5fe-126">-目的地</span><span class="sxs-lookup"><span data-stu-id="5f5fe-126">-Destination</span></span>
<span data-ttu-id="5f5fe-127">已建立包含嵌套目錄結構之檔案 (的絕對路徑，) 其中的檔案)  (將會上傳到 VM 中。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-127">The absolute path to a file (with nested directory structures already created) where the file (from sourceUri) will be uploaded to in the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: FileCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f5fe-128">-FileCustomizer</span><span class="sxs-lookup"><span data-stu-id="5f5fe-128">-FileCustomizer</span></span>
<span data-ttu-id="5f5fe-129">將檔案上傳至 (Linux、Windows) 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-129">Uploads files to VMs (Linux, Windows).</span></span>
<span data-ttu-id="5f5fe-130">對應至 Packer 檔案 provisioner。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-130">Corresponds to Packer file provisioner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FileCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f5fe-131">-篩選</span><span class="sxs-lookup"><span data-stu-id="5f5fe-131">-Filter</span></span>
<span data-ttu-id="5f5fe-132">要選取要套用之更新的篩選陣列。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-132">Array of filters to select updates to apply.</span></span>
<span data-ttu-id="5f5fe-133">省略或指定空陣列以使用預設 (無篩選) 。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-133">Omit or specify empty array to use the default (no filter).</span></span>
<span data-ttu-id="5f5fe-134">請參閱上方連結，以取得此欄位的範例和詳細描述。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-134">Refer to above link for examples and detailed description of this field.</span></span>

```yaml
Type: System.String[]
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f5fe-135">-內嵌</span><span class="sxs-lookup"><span data-stu-id="5f5fe-135">-Inline</span></span>
<span data-ttu-id="5f5fe-136">要執行的 shell 命令陣列。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-136">Array of shell commands to execute.</span></span>

```yaml
Type: System.String[]
Parameter Sets: PowerShellCustomizer, ShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f5fe-137">-PowerShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="5f5fe-137">-PowerShellCustomizer</span></span>
<span data-ttu-id="5f5fe-138">在 VM 上執行指定的 PowerShell (Windows) 。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-138">Runs the specified PowerShell on the VM (Windows).</span></span>
<span data-ttu-id="5f5fe-139">對應至 Packer powershell provisioner。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-139">Corresponds to Packer powershell provisioner.</span></span>
<span data-ttu-id="5f5fe-140">只能指定 [scriptUri] 或 "inline" 中的一個。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-140">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PowerShellCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f5fe-141">-RestartCheckCommand</span><span class="sxs-lookup"><span data-stu-id="5f5fe-141">-RestartCheckCommand</span></span>
<span data-ttu-id="5f5fe-142">要檢查重新開機成功的命令 [預設值： ' "」。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-142">Command to check if restart succeeded [Default: ''].</span></span>

```yaml
Type: System.String
Parameter Sets: RestartCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f5fe-143">-RestartCommand</span><span class="sxs-lookup"><span data-stu-id="5f5fe-143">-RestartCommand</span></span>
<span data-ttu-id="5f5fe-144">執行重新開機的命令 [預設：「關閉/r/f/t 0/c packer 重新開機」」</span><span class="sxs-lookup"><span data-stu-id="5f5fe-144">Command to execute the restart [Default: 'shutdown /r /f /t 0 /c packer restart']</span></span>

```yaml
Type: System.String
Parameter Sets: RestartCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f5fe-145">-RestartCustomizer</span><span class="sxs-lookup"><span data-stu-id="5f5fe-145">-RestartCustomizer</span></span>
<span data-ttu-id="5f5fe-146">重新開機 VM，然後等到它重新連線 (Windows) 。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-146">Reboots a VM and waits for it to come back online (Windows).</span></span>
<span data-ttu-id="5f5fe-147">對應至 Packer windows-重新開機 provisioner。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-147">Corresponds to Packer windows-restart provisioner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestartCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f5fe-148">-RestartTimeout</span><span class="sxs-lookup"><span data-stu-id="5f5fe-148">-RestartTimeout</span></span>
<span data-ttu-id="5f5fe-149">重新開機超時指定為數量級和 unit 的字串，例如 "5m" (5 分鐘) 或 "下半年" (2 小時) [預設值： ' 5m」]。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-149">Restart timeout specified as a string of magnitude and unit, e.g. '5m' (5 minutes) or '2h' (2 hours) [Default: '5m'].</span></span>

```yaml
Type: System.String
Parameter Sets: RestartCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f5fe-150">-RunElevated</span><span class="sxs-lookup"><span data-stu-id="5f5fe-150">-RunElevated</span></span>
<span data-ttu-id="5f5fe-151">如果已指定，就會使用較高的許可權來執行 PowerShell 腳本。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-151">If specified, the PowerShell script will be run with elevated privileges.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: PowerShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f5fe-152">-ScriptUri</span><span class="sxs-lookup"><span data-stu-id="5f5fe-152">-ScriptUri</span></span>
<span data-ttu-id="5f5fe-153">要執行以進行自訂的 shell 腳本 URI。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-153">URI of the shell script to be run for customizing.</span></span>
<span data-ttu-id="5f5fe-154">它可以是 github 連結、Azure 儲存空間的 SAS URI 等。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-154">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerShellCustomizer, ShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f5fe-155">-SearchCriterion</span><span class="sxs-lookup"><span data-stu-id="5f5fe-155">-SearchCriterion</span></span>
<span data-ttu-id="5f5fe-156">搜尋更新的準則。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-156">Criteria to search updates.</span></span>
<span data-ttu-id="5f5fe-157">省略或指定空字串，以使用預設 (搜尋所有) 。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-157">Omit or specify empty string to use the default (search all).</span></span>
<span data-ttu-id="5f5fe-158">請參閱上方連結，以取得此欄位的範例和詳細描述。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-158">Refer to above link for examples and detailed description of this field.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f5fe-159">-Sha256Checksum</span><span class="sxs-lookup"><span data-stu-id="5f5fe-159">-Sha256Checksum</span></span>
<span data-ttu-id="5f5fe-160">ScriptUri 欄位中提供之 shell 腳本的 SHA256 校驗和。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-160">SHA256 checksum of the shell script provided in the scriptUri field.</span></span>

```yaml
Type: System.String
Parameter Sets: FileCustomizer, PowerShellCustomizer, ShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f5fe-161">-ShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="5f5fe-161">-ShellCustomizer</span></span>
<span data-ttu-id="5f5fe-162">在自訂階段 (Linux) 中執行 shell 腳本。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-162">Runs a shell script during the customization phase (Linux).</span></span>
<span data-ttu-id="5f5fe-163">對應至 Packer shell provisioner。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-163">Corresponds to Packer shell provisioner.</span></span>
<span data-ttu-id="5f5fe-164">只能指定 [scriptUri] 或 "inline" 中的一個。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-164">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ShellCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f5fe-165">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="5f5fe-165">-SourceUri</span></span>
<span data-ttu-id="5f5fe-166">要上傳以自訂 VM 之檔案的 URI。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-166">The URI of the file to be uploaded for customizing the VM.</span></span>
<span data-ttu-id="5f5fe-167">它可以是 github 連結、Azure 儲存空間的 SAS URI 等。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-167">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: FileCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f5fe-168">-UpdateLimit</span><span class="sxs-lookup"><span data-stu-id="5f5fe-168">-UpdateLimit</span></span>
<span data-ttu-id="5f5fe-169">一次套用的更新數目上限。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-169">Maximum number of updates to apply at a time.</span></span>
<span data-ttu-id="5f5fe-170">省略或指定0，以使用預設 (1000) 。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-170">Omit or specify 0 to use the default (1000).</span></span>

```yaml
Type: System.Int32
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f5fe-171">-ValidExitCode</span><span class="sxs-lookup"><span data-stu-id="5f5fe-171">-ValidExitCode</span></span>
<span data-ttu-id="5f5fe-172">PowerShell 腳本的有效結束碼。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-172">Valid exit codes for the PowerShell script.</span></span>
<span data-ttu-id="5f5fe-173">[預設值： 0]。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-173">[Default: 0].</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: PowerShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f5fe-174">-WindowsUpdateCustomizer</span><span class="sxs-lookup"><span data-stu-id="5f5fe-174">-WindowsUpdateCustomizer</span></span>
<span data-ttu-id="5f5fe-175">安裝 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-175">Installs Windows Updates.</span></span>
<span data-ttu-id="5f5fe-176">對應至 Packer [Windows Update Provisioner] (https://github.com/rgl/packer-provisioner-windows-update) 。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-176">Corresponds to Packer Windows Update Provisioner (https://github.com/rgl/packer-provisioner-windows-update).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f5fe-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f5fe-177">CommonParameters</span></span>
<span data-ttu-id="5f5fe-178">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f5fe-179">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f5fe-180">輸入</span><span class="sxs-lookup"><span data-stu-id="5f5fe-180">INPUTS</span></span>

## <span data-ttu-id="5f5fe-181">輸出</span><span class="sxs-lookup"><span data-stu-id="5f5fe-181">OUTPUTS</span></span>

### <span data-ttu-id="5f5fe-182">IImageTemplateCustomizer （ImageBuilder）。 Api20200214。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-182">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateCustomizer</span></span>

## <span data-ttu-id="5f5fe-183">筆記</span><span class="sxs-lookup"><span data-stu-id="5f5fe-183">NOTES</span></span>

<span data-ttu-id="5f5fe-184">別名</span><span class="sxs-lookup"><span data-stu-id="5f5fe-184">ALIASES</span></span>

## <span data-ttu-id="5f5fe-185">相關連結</span><span class="sxs-lookup"><span data-stu-id="5f5fe-185">RELATED LINKS</span></span>

