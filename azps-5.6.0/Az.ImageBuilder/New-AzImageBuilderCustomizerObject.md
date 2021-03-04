---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/new-AzImageBuilderCustomizerObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
ms.openlocfilehash: 97e59efcc20f8ce025b2e90285ef051edc8272dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917186"
---
# <span data-ttu-id="ab161-101">New-AzImageBuilderCustomizerObject</span><span class="sxs-lookup"><span data-stu-id="ab161-101">New-AzImageBuilderCustomizerObject</span></span>

## <span data-ttu-id="ab161-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ab161-102">SYNOPSIS</span></span>
<span data-ttu-id="ab161-103">說明圖像自訂的單位</span><span class="sxs-lookup"><span data-stu-id="ab161-103">Describes a unit of image customization</span></span>

## <span data-ttu-id="ab161-104">語法</span><span class="sxs-lookup"><span data-stu-id="ab161-104">SYNTAX</span></span>

### <span data-ttu-id="ab161-105">ShellCustomizer (預設) </span><span class="sxs-lookup"><span data-stu-id="ab161-105">ShellCustomizer (Default)</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -ShellCustomizer [-Inline <String[]>]
 [-ScriptUri <String>] [-Sha256Checksum <String>] [<CommonParameters>]
```

### <span data-ttu-id="ab161-106">FileCustomizer</span><span class="sxs-lookup"><span data-stu-id="ab161-106">FileCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -FileCustomizer [-Destination <String>]
 [-Sha256Checksum <String>] [-SourceUri <String>] [<CommonParameters>]
```

### <span data-ttu-id="ab161-107">PowerShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="ab161-107">PowerShellCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -PowerShellCustomizer [-Inline <String[]>]
 [-RunElevated <Boolean>] [-ScriptUri <String>] [-Sha256Checksum <String>] [-ValidExitCode <Int32[]>]
 [<CommonParameters>]
```

### <span data-ttu-id="ab161-108">重新開機自訂程式</span><span class="sxs-lookup"><span data-stu-id="ab161-108">RestartCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -RestartCustomizer [-RestartCheckCommand <String>]
 [-RestartCommand <String>] [-RestartTimeout <String>] [<CommonParameters>]
```

### <span data-ttu-id="ab161-109">WindowsUpdateCustomizer</span><span class="sxs-lookup"><span data-stu-id="ab161-109">WindowsUpdateCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -WindowsUpdateCustomizer [-Filter <String[]>]
 [-SearchCriterion <String>] [-UpdateLimit <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="ab161-110">描述</span><span class="sxs-lookup"><span data-stu-id="ab161-110">DESCRIPTION</span></span>
<span data-ttu-id="ab161-111">說明圖像自訂的單位</span><span class="sxs-lookup"><span data-stu-id="ab161-111">Describes a unit of image customization</span></span>

## <span data-ttu-id="ab161-112">例子</span><span class="sxs-lookup"><span data-stu-id="ab161-112">EXAMPLES</span></span>

### <span data-ttu-id="ab161-113">範例 1：建立 Windows 更新自訂程式</span><span class="sxs-lookup"><span data-stu-id="ab161-113">Example 1: Create a windows update customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -WindowsUpdateCustomizer -Filter ("BrowseOnly", "IsInstalled") -SearchCriterion "BrowseOnly=0 and IsInstalled=0"  -UpdateLimit 100 -CustomizerName 'WindUpdate'

Name       Type          Filter                    SearchCriterion                UpdateLimit
----       ----          ------                    ---------------                -----------
WindUpdate WindowsUpdate {BrowseOnly, IsInstalled} BrowseOnly=0 and IsInstalled=0 100
```

<span data-ttu-id="ab161-114">此命令會建立 Windows 更新自訂程式。</span><span class="sxs-lookup"><span data-stu-id="ab161-114">This command creates a windows update customizer.</span></span>

### <span data-ttu-id="ab161-115">範例 2：建立檔案自訂程式</span><span class="sxs-lookup"><span data-stu-id="ab161-115">Example 2: Create a file customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -FileCustomizer -CustomizerName 'filecus' -Destination 'c:\\buildArtifacts\\index.html' -SourceUri 'https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/index.html'

Name    Type Destination                    Sha256Checksum SourceUri
----    ---- -----------                    -------------- ---------
filecus File c:\\buildArtifacts\\index.html                https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/…

```

<span data-ttu-id="ab161-116">此命令會建立檔案自訂程式。</span><span class="sxs-lookup"><span data-stu-id="ab161-116">This command creates a file customizer.</span></span>

### <span data-ttu-id="ab161-117">範例 3：建立 Powershell 自訂程式</span><span class="sxs-lookup"><span data-stu-id="ab161-117">Example 3: Create a powershell customizer</span></span>
```powershell
PS C:\> $inline = @("mkdir c:\\buildActions", "echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt")
PS C:\> New-AzImageBuilderCustomizerObject -PowerShellCustomizer -CustomizerName settingUpMgmtAgtPath -RunElevated $false -Inline $inline

Name                 Type       Inline                                                                                                  RunElevated ScriptUri Sha256Checksum
----                 ----       ------                                                                                                  ----------- --------- --------------
settingUpMgmtAgtPath PowerShell {mkdir c:\\buildActions, echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt} False

```

<span data-ttu-id="ab161-118">此命令會建立 Powershell 自訂程式。</span><span class="sxs-lookup"><span data-stu-id="ab161-118">This command creates a powershell customizer.</span></span>

### <span data-ttu-id="ab161-119">範例 4：建立重新開機自訂程式</span><span class="sxs-lookup"><span data-stu-id="ab161-119">Example 4: Create a restart customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -RestartCustomizer -CustomizerName 'restcus' -RestartCommand 'shutdown /f /r /t 0 /c \"packer restart\"' -RestartCheckCommand 'powershell -command "& {Write-Output "restarted."}"' -RestartTimeout '10m'

Name    Type           RestartCheckCommand                                 RestartCommand                            RestartTimeout
----    ----           -------------------                                 --------------                            --------------
restcus WindowsRestart powershell -command "& {Write-Output "restarted."}" shutdown /f /r /t 0 /c \"packer restart\" 10m
```

<span data-ttu-id="ab161-120">此命令會建立重新開機自訂程式。</span><span class="sxs-lookup"><span data-stu-id="ab161-120">This command creates a restart customizer.</span></span>

### <span data-ttu-id="ab161-121">範例 5：建立 shell 自訂程式</span><span class="sxs-lookup"><span data-stu-id="ab161-121">Example 5: Create a shell customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -ShellCustomizer -CustomizerName downloadBuildArtifacts -ScriptUri "https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh" 

Name                   Type  Inline ScriptUri                                                                                                      Sha256Checksum
----                   ----  ------ ---------                                                                                                      --------------
downloadBuildArtifacts Shell        https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh
```

<span data-ttu-id="ab161-122">此命令會建立命令命令自訂程式。</span><span class="sxs-lookup"><span data-stu-id="ab161-122">This command creates a shell customizer.</span></span>

## <span data-ttu-id="ab161-123">參數</span><span class="sxs-lookup"><span data-stu-id="ab161-123">PARAMETERS</span></span>

### <span data-ttu-id="ab161-124">-CustomizerName</span><span class="sxs-lookup"><span data-stu-id="ab161-124">-CustomizerName</span></span>
<span data-ttu-id="ab161-125">好用名稱，提供此自訂步驟的上下文。</span><span class="sxs-lookup"><span data-stu-id="ab161-125">Friendly Name to provide context on what this customization step does.</span></span>

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

### <span data-ttu-id="ab161-126">-目的地</span><span class="sxs-lookup"><span data-stu-id="ab161-126">-Destination</span></span>
<span data-ttu-id="ab161-127">已建立巢 (目錄結構的檔案絕對路徑) 來源Uri (檔案) 上傳至 VM。</span><span class="sxs-lookup"><span data-stu-id="ab161-127">The absolute path to a file (with nested directory structures already created) where the file (from sourceUri) will be uploaded to in the VM.</span></span>

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

### <span data-ttu-id="ab161-128">-FileCustomizer</span><span class="sxs-lookup"><span data-stu-id="ab161-128">-FileCustomizer</span></span>
<span data-ttu-id="ab161-129">將檔案上傳到 Linux (Windows) 。</span><span class="sxs-lookup"><span data-stu-id="ab161-129">Uploads files to VMs (Linux, Windows).</span></span>
<span data-ttu-id="ab161-130">對應到 Packer 檔案提供器。</span><span class="sxs-lookup"><span data-stu-id="ab161-130">Corresponds to Packer file provisioner.</span></span>

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

### <span data-ttu-id="ab161-131">-篩選</span><span class="sxs-lookup"><span data-stu-id="ab161-131">-Filter</span></span>
<span data-ttu-id="ab161-132">要選取要申請之更新的篩選陣列。</span><span class="sxs-lookup"><span data-stu-id="ab161-132">Array of filters to select updates to apply.</span></span>
<span data-ttu-id="ab161-133">省略或指定空白陣列，以使用預設 (篩選) 。</span><span class="sxs-lookup"><span data-stu-id="ab161-133">Omit or specify empty array to use the default (no filter).</span></span>
<span data-ttu-id="ab161-134">請參閱上述連結以瞭解此欄位的範例和詳細描述。</span><span class="sxs-lookup"><span data-stu-id="ab161-134">Refer to above link for examples and detailed description of this field.</span></span>

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

### <span data-ttu-id="ab161-135">-內嵌</span><span class="sxs-lookup"><span data-stu-id="ab161-135">-Inline</span></span>
<span data-ttu-id="ab161-136">要執行的 shell 命令陣列。</span><span class="sxs-lookup"><span data-stu-id="ab161-136">Array of shell commands to execute.</span></span>

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

### <span data-ttu-id="ab161-137">-PowerShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="ab161-137">-PowerShellCustomizer</span></span>
<span data-ttu-id="ab161-138">在 Windows 應用程式上的 VM (執行) 。</span><span class="sxs-lookup"><span data-stu-id="ab161-138">Runs the specified PowerShell on the VM (Windows).</span></span>
<span data-ttu-id="ab161-139">對應到 Packer Powershell 提供器。</span><span class="sxs-lookup"><span data-stu-id="ab161-139">Corresponds to Packer powershell provisioner.</span></span>
<span data-ttu-id="ab161-140">您可以指定其中一個"scriptUri"或"內嵌」。</span><span class="sxs-lookup"><span data-stu-id="ab161-140">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

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

### <span data-ttu-id="ab161-141">-RestartCheckCommand</span><span class="sxs-lookup"><span data-stu-id="ab161-141">-RestartCheckCommand</span></span>
<span data-ttu-id="ab161-142">檢查重新開機是否成功的命令 [預設： '']。</span><span class="sxs-lookup"><span data-stu-id="ab161-142">Command to check if restart succeeded [Default: ''].</span></span>

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

### <span data-ttu-id="ab161-143">-RestartCommand</span><span class="sxs-lookup"><span data-stu-id="ab161-143">-RestartCommand</span></span>
<span data-ttu-id="ab161-144">執行重新開機的命令 [預設： '關機 /r /f /t 0 /c packer 重新開機']</span><span class="sxs-lookup"><span data-stu-id="ab161-144">Command to execute the restart [Default: 'shutdown /r /f /t 0 /c packer restart']</span></span>

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

### <span data-ttu-id="ab161-145">-重新開機自訂器</span><span class="sxs-lookup"><span data-stu-id="ab161-145">-RestartCustomizer</span></span>
<span data-ttu-id="ab161-146">重新開機 VM，並等待它回到 Windows (上) 。</span><span class="sxs-lookup"><span data-stu-id="ab161-146">Reboots a VM and waits for it to come back online (Windows).</span></span>
<span data-ttu-id="ab161-147">對應到 Packer Windows-restart 提供器。</span><span class="sxs-lookup"><span data-stu-id="ab161-147">Corresponds to Packer windows-restart provisioner.</span></span>

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

### <span data-ttu-id="ab161-148">-RestartTimeout</span><span class="sxs-lookup"><span data-stu-id="ab161-148">-RestartTimeout</span></span>
<span data-ttu-id="ab161-149">重新開機超時指定為量級和單位字串，例如 '5m' (5 分鐘) 或 '2h' (2 小時) [預設： '5m']。</span><span class="sxs-lookup"><span data-stu-id="ab161-149">Restart timeout specified as a string of magnitude and unit, e.g. '5m' (5 minutes) or '2h' (2 hours) [Default: '5m'].</span></span>

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

### <span data-ttu-id="ab161-150">-RunEated</span><span class="sxs-lookup"><span data-stu-id="ab161-150">-RunElevated</span></span>
<span data-ttu-id="ab161-151">如果指定，PowerShell 腳本會以較高的權限執行。</span><span class="sxs-lookup"><span data-stu-id="ab161-151">If specified, the PowerShell script will be run with elevated privileges.</span></span>

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

### <span data-ttu-id="ab161-152">-ScriptUri</span><span class="sxs-lookup"><span data-stu-id="ab161-152">-ScriptUri</span></span>
<span data-ttu-id="ab161-153">要執行自訂之 shell 腳本的 URI。</span><span class="sxs-lookup"><span data-stu-id="ab161-153">URI of the shell script to be run for customizing.</span></span>
<span data-ttu-id="ab161-154">它可以是 github 連結、AZURE 儲存空間的 SAS URI 等等。</span><span class="sxs-lookup"><span data-stu-id="ab161-154">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

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

### <span data-ttu-id="ab161-155">-SearchCriterion</span><span class="sxs-lookup"><span data-stu-id="ab161-155">-SearchCriterion</span></span>
<span data-ttu-id="ab161-156">搜尋更新的準則。</span><span class="sxs-lookup"><span data-stu-id="ab161-156">Criteria to search updates.</span></span>
<span data-ttu-id="ab161-157">省略或指定空字串，以使用預設 (搜尋所有) 。</span><span class="sxs-lookup"><span data-stu-id="ab161-157">Omit or specify empty string to use the default (search all).</span></span>
<span data-ttu-id="ab161-158">請參閱上述連結以瞭解此欄位的範例和詳細描述。</span><span class="sxs-lookup"><span data-stu-id="ab161-158">Refer to above link for examples and detailed description of this field.</span></span>

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

### <span data-ttu-id="ab161-159">-Sha256Checksum</span><span class="sxs-lookup"><span data-stu-id="ab161-159">-Sha256Checksum</span></span>
<span data-ttu-id="ab161-160">SCRIPTUri 功能變數中提供的 shell 腳本 SHA256 檢查和。</span><span class="sxs-lookup"><span data-stu-id="ab161-160">SHA256 checksum of the shell script provided in the scriptUri field.</span></span>

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

### <span data-ttu-id="ab161-161">-ShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="ab161-161">-ShellCustomizer</span></span>
<span data-ttu-id="ab161-162">在 Linux (自訂階段期間執行 shell) 。</span><span class="sxs-lookup"><span data-stu-id="ab161-162">Runs a shell script during the customization phase (Linux).</span></span>
<span data-ttu-id="ab161-163">對應到 Packer Shell 提供器。</span><span class="sxs-lookup"><span data-stu-id="ab161-163">Corresponds to Packer shell provisioner.</span></span>
<span data-ttu-id="ab161-164">您可以指定其中一個"scriptUri"或"內嵌」。</span><span class="sxs-lookup"><span data-stu-id="ab161-164">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

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

### <span data-ttu-id="ab161-165">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="ab161-165">-SourceUri</span></span>
<span data-ttu-id="ab161-166">要上傳以自訂 VM 的檔案 URI。</span><span class="sxs-lookup"><span data-stu-id="ab161-166">The URI of the file to be uploaded for customizing the VM.</span></span>
<span data-ttu-id="ab161-167">它可以是 github 連結、AZURE 儲存空間的 SAS URI 等等。</span><span class="sxs-lookup"><span data-stu-id="ab161-167">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

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

### <span data-ttu-id="ab161-168">-UpdateLimit</span><span class="sxs-lookup"><span data-stu-id="ab161-168">-UpdateLimit</span></span>
<span data-ttu-id="ab161-169">一次要申請的更新數目上限。</span><span class="sxs-lookup"><span data-stu-id="ab161-169">Maximum number of updates to apply at a time.</span></span>
<span data-ttu-id="ab161-170">省略或指定 0 以使用預設 (1000) 。</span><span class="sxs-lookup"><span data-stu-id="ab161-170">Omit or specify 0 to use the default (1000).</span></span>

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

### <span data-ttu-id="ab161-171">-ValidExitCode</span><span class="sxs-lookup"><span data-stu-id="ab161-171">-ValidExitCode</span></span>
<span data-ttu-id="ab161-172">PowerShell 腳本的有效離開代碼。</span><span class="sxs-lookup"><span data-stu-id="ab161-172">Valid exit codes for the PowerShell script.</span></span>
<span data-ttu-id="ab161-173">[預設：0]。</span><span class="sxs-lookup"><span data-stu-id="ab161-173">[Default: 0].</span></span>

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

### <span data-ttu-id="ab161-174">-WindowsUpdateCustomizer</span><span class="sxs-lookup"><span data-stu-id="ab161-174">-WindowsUpdateCustomizer</span></span>
<span data-ttu-id="ab161-175">安裝 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="ab161-175">Installs Windows Updates.</span></span>
<span data-ttu-id="ab161-176">對應至 Packer Windows Update Provisioner https://github.com/rgl/packer-provisioner-windows-update) (。</span><span class="sxs-lookup"><span data-stu-id="ab161-176">Corresponds to Packer Windows Update Provisioner (https://github.com/rgl/packer-provisioner-windows-update).</span></span>

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

### <span data-ttu-id="ab161-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab161-177">CommonParameters</span></span>
<span data-ttu-id="ab161-178">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ab161-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab161-179">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ab161-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab161-180">輸入</span><span class="sxs-lookup"><span data-stu-id="ab161-180">INPUTS</span></span>

## <span data-ttu-id="ab161-181">輸出</span><span class="sxs-lookup"><span data-stu-id="ab161-181">OUTPUTS</span></span>

### <span data-ttu-id="ab161-182">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateCustomizer</span><span class="sxs-lookup"><span data-stu-id="ab161-182">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateCustomizer</span></span>

## <span data-ttu-id="ab161-183">筆記</span><span class="sxs-lookup"><span data-stu-id="ab161-183">NOTES</span></span>

<span data-ttu-id="ab161-184">別名</span><span class="sxs-lookup"><span data-stu-id="ab161-184">ALIASES</span></span>

## <span data-ttu-id="ab161-185">相關連結</span><span class="sxs-lookup"><span data-stu-id="ab161-185">RELATED LINKS</span></span>

