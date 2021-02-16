---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/New-AzImageBuilderTemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderTemplate.md
ms.openlocfilehash: 337584fb7f960f64ee94c5206f9bf60b0cc6c21a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131903"
---
# <span data-ttu-id="3ec5e-101">New-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="3ec5e-101">New-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="3ec5e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3ec5e-102">SYNOPSIS</span></span>
<span data-ttu-id="3ec5e-103">建立虛擬機器影像範本</span><span class="sxs-lookup"><span data-stu-id="3ec5e-103">Create a virtual machine image template</span></span>

## <span data-ttu-id="3ec5e-104">句法</span><span class="sxs-lookup"><span data-stu-id="3ec5e-104">SYNTAX</span></span>

```
New-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 -Distribute <IImageTemplateDistributor[]> -Source <IImageTemplateSource> -UserAssignedIdentityId <String>
 [-SubscriptionId <String>] [-BuildTimeoutInMinute <Int32>] [-Customize <IImageTemplateCustomizer[]>]
 [-LastRunStatusEndTime <DateTime>] [-LastRunStatusMessage <String>] [-LastRunStatusRunState <RunState>]
 [-LastRunStatusRunSubState <RunSubState>] [-LastRunStatusStartTime <DateTime>] [-Location <String>]
 [-ProvisioningErrorCode <ProvisioningErrorCode>] [-ProvisioningErrorMessage <String>] [-Tag <Hashtable>]
 [-VMProfileOsdiskSizeInGb <Int32>] [-VMProfileVmSize <String>] [-VnetConfigSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3ec5e-105">說明</span><span class="sxs-lookup"><span data-stu-id="3ec5e-105">DESCRIPTION</span></span>
<span data-ttu-id="3ec5e-106">建立虛擬機器影像範本</span><span class="sxs-lookup"><span data-stu-id="3ec5e-106">Create a virtual machine image template</span></span>

## <span data-ttu-id="3ec5e-107">示例</span><span class="sxs-lookup"><span data-stu-id="3ec5e-107">EXAMPLES</span></span>

### <span data-ttu-id="3ec5e-108">範例1：建立虛擬機器影像範本</span><span class="sxs-lookup"><span data-stu-id="3ec5e-108">Example 1: Create a virtual machine image template</span></span>
```powershell
PS C:\> $srcPlatform = New-AzImageBuilderSourceObject -SourceTypePlatformImage -Publisher 'Canonical'  -Offer 'UbuntuServer' -Sku '18.04-LTS' -Version 'latest'
PS C:\> $disSharedImg = New-AzImageBuilderDistributorObject -SharedImageDistributor -ArtifactTag @{tag='dis-share'} -GalleryImageId '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/testsharedgallery/images/imagedefinition-linux/versions/1.0.0' -ReplicationRegion 'eastus2' -RunOutputName 'runoutput-01'  -ExcludeFromLatest $false
PS C:\> $customizer = New-AzImageBuilderCustomizerObject -ShellCustomizer -CustomizerName 'CheckSumCompareShellScript' -ScriptUri 'https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh' -Sha256Checksum 'ade4c5214c3c675e92c66e2d067a870c5b81b9844b3de3cc72c49ff36425fc93'
PS C:\> $userAssignedIdentity = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/wyunchi-imagebuilder/providers/Microsoft.ManagedIdentity/userAssignedIdentities/image-builder-user-assign-identity'
PS C:\> New-AzImageBuilderTemplate -ImageTemplateName platform-shared-img -ResourceGroupName wyunchi-imagebuilder -Source $srcPlatform -Distribute $disSharedImg -Customize $customizer -Location eastus  -UserAssignedIdentityId $userAssignedIdentity

Location Name                Type
-------- ----                ----
PlanInfoPlanName      :
PlanInfoPlanPublisher :
Sku                   : 18.04-LTS
Version               : latest
PlanInfo              : Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.PlatformImagePurchasePlan
```

<span data-ttu-id="3ec5e-109">這個命令會建立虛擬機器影像範本。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-109">This commands creates a virtual machine image template.</span></span>

## <span data-ttu-id="3ec5e-110">參數</span><span class="sxs-lookup"><span data-stu-id="3ec5e-110">PARAMETERS</span></span>

### <span data-ttu-id="3ec5e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ec5e-111">-AsJob</span></span>
<span data-ttu-id="3ec5e-112">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="3ec5e-112">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec5e-113">-BuildTimeoutInMinute</span><span class="sxs-lookup"><span data-stu-id="3ec5e-113">-BuildTimeoutInMinute</span></span>
<span data-ttu-id="3ec5e-114">建立影像範本時所要等待的最大持續時間。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-114">Maximum duration to wait while building the image template.</span></span>
<span data-ttu-id="3ec5e-115">省略或指定0，以使用預設 (4 小時) 。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-115">Omit or specify 0 to use the default (4 hours).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec5e-116">-自訂</span><span class="sxs-lookup"><span data-stu-id="3ec5e-116">-Customize</span></span>
<span data-ttu-id="3ec5e-117">指定用來描述影像之自訂步驟的屬性，例如影像來源等。若要建立，請參閱自訂屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-117">Specifies the properties used to describe the customization steps of the image, like Image source etc. To construct, see NOTES section for CUSTOMIZE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateCustomizer[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec5e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ec5e-118">-DefaultProfile</span></span>
<span data-ttu-id="3ec5e-119">地區 HideParameter 用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-119">region HideParameter The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec5e-120">-發佈</span><span class="sxs-lookup"><span data-stu-id="3ec5e-120">-Distribute</span></span>
<span data-ttu-id="3ec5e-121">需要移至圖像輸出的分佈目標。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-121">The distribution targets where the image output needs to go to.</span></span>
<span data-ttu-id="3ec5e-122">若要建立，請參閱發佈屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-122">To construct, see NOTES section for DISTRIBUTE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateDistributor[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec5e-123">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="3ec5e-123">-ImageTemplateName</span></span>
<span data-ttu-id="3ec5e-124">影像範本的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-124">The name of the image Template.</span></span>

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

### <span data-ttu-id="3ec5e-125">-LastRunStatusEndTime</span><span class="sxs-lookup"><span data-stu-id="3ec5e-125">-LastRunStatusEndTime</span></span>
<span data-ttu-id="3ec5e-126">上次執行 (UTC) 的結束時間。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-126">End time of the last run (UTC).</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec5e-127">-LastRunStatusMessage</span><span class="sxs-lookup"><span data-stu-id="3ec5e-127">-LastRunStatusMessage</span></span>
<span data-ttu-id="3ec5e-128">關於上次執行狀態的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-128">Verbose information about the last run state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec5e-129">-LastRunStatusRunState</span><span class="sxs-lookup"><span data-stu-id="3ec5e-129">-LastRunStatusRunState</span></span>
<span data-ttu-id="3ec5e-130">上次執行的狀態。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-130">State of the last run.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.RunState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec5e-131">-LastRunStatusRunSubState</span><span class="sxs-lookup"><span data-stu-id="3ec5e-131">-LastRunStatusRunSubState</span></span>
<span data-ttu-id="3ec5e-132">最後一次執行的子狀態。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-132">Sub-state of the last run.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.RunSubState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec5e-133">-LastRunStatusStartTime</span><span class="sxs-lookup"><span data-stu-id="3ec5e-133">-LastRunStatusStartTime</span></span>
<span data-ttu-id="3ec5e-134">上次執行 (UTC) 的開始時間。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-134">Start time of the last run (UTC).</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec5e-135">-位置</span><span class="sxs-lookup"><span data-stu-id="3ec5e-135">-Location</span></span>
<span data-ttu-id="3ec5e-136">資源位置。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-136">Resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec5e-137">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3ec5e-137">-NoWait</span></span>
<span data-ttu-id="3ec5e-138">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="3ec5e-138">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec5e-139">-ProvisioningErrorCode</span><span class="sxs-lookup"><span data-stu-id="3ec5e-139">-ProvisioningErrorCode</span></span>
<span data-ttu-id="3ec5e-140">置備失敗的錯誤代碼。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-140">Error code of the provisioning failure.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.ProvisioningErrorCode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec5e-141">-ProvisioningErrorMessage</span><span class="sxs-lookup"><span data-stu-id="3ec5e-141">-ProvisioningErrorMessage</span></span>
<span data-ttu-id="3ec5e-142">有關預配失敗的詳細錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-142">Verbose error message about the provisioning failure.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec5e-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ec5e-143">-ResourceGroupName</span></span>
<span data-ttu-id="3ec5e-144">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-144">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec5e-145">-來源</span><span class="sxs-lookup"><span data-stu-id="3ec5e-145">-Source</span></span>
<span data-ttu-id="3ec5e-146">描述建立、自訂及發佈的虛擬機器影像來源。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-146">Describes a virtual machine image source for building, customizing and distributing.</span></span>
<span data-ttu-id="3ec5e-147">若要建立，請參閱來源屬性的記事區段，並建立雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-147">To construct, see NOTES section for SOURCE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec5e-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3ec5e-148">-SubscriptionId</span></span>
<span data-ttu-id="3ec5e-149">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-149">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec5e-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="3ec5e-150">-Tag</span></span>
<span data-ttu-id="3ec5e-151">資源標記。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-151">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec5e-152">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="3ec5e-152">-UserAssignedIdentityId</span></span>
<span data-ttu-id="3ec5e-153">指派身分識別的使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-153">The id of user assigned identity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec5e-154">-VMProfileOsdiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="3ec5e-154">-VMProfileOsdiskSizeInGb</span></span>
<span data-ttu-id="3ec5e-155">OS 磁片大小（GB）。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-155">Size of the OS disk in GB.</span></span>
<span data-ttu-id="3ec5e-156">省略或指定0以使用 Azure 的預設作業系統磁片大小。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-156">Omit or specify 0 to use Azure's default OS disk size.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec5e-157">-VMProfileVmSize</span><span class="sxs-lookup"><span data-stu-id="3ec5e-157">-VMProfileVmSize</span></span>
<span data-ttu-id="3ec5e-158">用來建立、自訂及捕獲影像的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-158">Size of the virtual machine used to build, customize and capture images.</span></span>
<span data-ttu-id="3ec5e-159">省略或指定空字串，以使用預設 (Standard_D1_v2) 。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-159">Omit or specify empty string to use the default (Standard_D1_v2).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec5e-160">-VnetConfigSubnetId</span><span class="sxs-lookup"><span data-stu-id="3ec5e-160">-VnetConfigSubnetId</span></span>
<span data-ttu-id="3ec5e-161">預先存在的子網的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-161">Resource id of a pre-existing subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec5e-162">-確認</span><span class="sxs-lookup"><span data-stu-id="3ec5e-162">-Confirm</span></span>
<span data-ttu-id="3ec5e-163">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-163">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec5e-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ec5e-164">-WhatIf</span></span>
<span data-ttu-id="3ec5e-165">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ec5e-166">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-166">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec5e-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ec5e-167">CommonParameters</span></span>
<span data-ttu-id="3ec5e-168">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ec5e-169">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ec5e-170">輸入</span><span class="sxs-lookup"><span data-stu-id="3ec5e-170">INPUTS</span></span>

## <span data-ttu-id="3ec5e-171">輸出</span><span class="sxs-lookup"><span data-stu-id="3ec5e-171">OUTPUTS</span></span>

### <span data-ttu-id="3ec5e-172">IImageTemplate （ImageBuilder）。 Api20200214。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-172">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span></span>

## <span data-ttu-id="3ec5e-173">筆記</span><span class="sxs-lookup"><span data-stu-id="3ec5e-173">NOTES</span></span>

<span data-ttu-id="3ec5e-174">別名</span><span class="sxs-lookup"><span data-stu-id="3ec5e-174">ALIASES</span></span>

<span data-ttu-id="3ec5e-175">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="3ec5e-175">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3ec5e-176">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-176">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3ec5e-177">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-177">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3ec5e-178">自訂 <IImageTemplateCustomizer [] >：指定用來描述影像之自訂步驟的屬性，例如影像來源等。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-178">CUSTOMIZE <IImageTemplateCustomizer[]>: Specifies the properties used to describe the customization steps of the image, like Image source etc.</span></span>
  - <span data-ttu-id="3ec5e-179">`Type <String>`：您想要在影像上使用的自訂工具類型。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-179">`Type <String>`: The type of customization tool you want to use on the Image.</span></span> <span data-ttu-id="3ec5e-180">例如，"Shell" 可以是 Shell 定制器</span><span class="sxs-lookup"><span data-stu-id="3ec5e-180">For example, "Shell" can be shell customizer</span></span>
  - <span data-ttu-id="3ec5e-181">`[Name <String>]`：易記的名稱，可提供此自訂步驟的功能內容</span><span class="sxs-lookup"><span data-stu-id="3ec5e-181">`[Name <String>]`: Friendly Name to provide context on what this customization step does</span></span>

<span data-ttu-id="3ec5e-182">發佈 <IImageTemplateDistributor [] >：分佈目標，圖像輸出需要移至該物件。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-182">DISTRIBUTE <IImageTemplateDistributor[]>: The distribution targets where the image output needs to go to.</span></span>
  - <span data-ttu-id="3ec5e-183">`RunOutputName <String>`：要用於關聯 RunOutput 的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-183">`RunOutputName <String>`: The name to be used for the associated RunOutput.</span></span>
  - <span data-ttu-id="3ec5e-184">`Type <String>`：發佈類型。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-184">`Type <String>`: Type of distribution.</span></span>
  - <span data-ttu-id="3ec5e-185">`[ArtifactTag <IImageTemplateDistributorArtifactTags>]`：由分銷商建立/更新後，會套用到專案的標記。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-185">`[ArtifactTag <IImageTemplateDistributorArtifactTags>]`: Tags that will be applied to the artifact once it has been created/updated by the distributor.</span></span>
    - <span data-ttu-id="3ec5e-186">`[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-186">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

<span data-ttu-id="3ec5e-187">來源 <IImageTemplateSource> ：說明建立、自訂及發佈的虛擬機器影像來源。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-187">SOURCE <IImageTemplateSource>: Describes a virtual machine image source for building, customizing and distributing.</span></span>
  - <span data-ttu-id="3ec5e-188">`Type <String>`：指定您要開始使用的來源影像類型。</span><span class="sxs-lookup"><span data-stu-id="3ec5e-188">`Type <String>`: Specifies the type of source image you want to start with.</span></span>

## <span data-ttu-id="3ec5e-189">相關連結</span><span class="sxs-lookup"><span data-stu-id="3ec5e-189">RELATED LINKS</span></span>

