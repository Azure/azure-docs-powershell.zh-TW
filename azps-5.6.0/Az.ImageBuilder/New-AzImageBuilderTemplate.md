---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/New-AzImageBuilderTemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderTemplate.md
ms.openlocfilehash: 98ef058c8a5110f7b97d794f7ebf41744ac12c2b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917181"
---
# <span data-ttu-id="f3d52-101">New-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="f3d52-101">New-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="f3d52-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f3d52-102">SYNOPSIS</span></span>
<span data-ttu-id="f3d52-103">建立虛擬機器映射範本</span><span class="sxs-lookup"><span data-stu-id="f3d52-103">Create a virtual machine image template</span></span>

## <span data-ttu-id="f3d52-104">語法</span><span class="sxs-lookup"><span data-stu-id="f3d52-104">SYNTAX</span></span>

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

## <span data-ttu-id="f3d52-105">描述</span><span class="sxs-lookup"><span data-stu-id="f3d52-105">DESCRIPTION</span></span>
<span data-ttu-id="f3d52-106">建立虛擬機器映射範本</span><span class="sxs-lookup"><span data-stu-id="f3d52-106">Create a virtual machine image template</span></span>

## <span data-ttu-id="f3d52-107">例子</span><span class="sxs-lookup"><span data-stu-id="f3d52-107">EXAMPLES</span></span>

### <span data-ttu-id="f3d52-108">範例 1：建立虛擬機器映射範本</span><span class="sxs-lookup"><span data-stu-id="f3d52-108">Example 1: Create a virtual machine image template</span></span>
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

<span data-ttu-id="f3d52-109">這個命令會建立虛擬機器映射範本。</span><span class="sxs-lookup"><span data-stu-id="f3d52-109">This commands creates a virtual machine image template.</span></span>

## <span data-ttu-id="f3d52-110">參數</span><span class="sxs-lookup"><span data-stu-id="f3d52-110">PARAMETERS</span></span>

### <span data-ttu-id="f3d52-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f3d52-111">-AsJob</span></span>
<span data-ttu-id="f3d52-112">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="f3d52-112">Run the command as a job</span></span>

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

### <span data-ttu-id="f3d52-113">-BuildTimeoutInMinute</span><span class="sxs-lookup"><span data-stu-id="f3d52-113">-BuildTimeoutInMinute</span></span>
<span data-ttu-id="f3d52-114">建立圖像範本時要等候的持續時間上限。</span><span class="sxs-lookup"><span data-stu-id="f3d52-114">Maximum duration to wait while building the image template.</span></span>
<span data-ttu-id="f3d52-115">省略或指定 0 以使用預設 (4 小時) 。</span><span class="sxs-lookup"><span data-stu-id="f3d52-115">Omit or specify 0 to use the default (4 hours).</span></span>

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

### <span data-ttu-id="f3d52-116">-自訂</span><span class="sxs-lookup"><span data-stu-id="f3d52-116">-Customize</span></span>
<span data-ttu-id="f3d52-117">指定用來描述影像自訂步驟的屬性，例如圖像來源等。若要建構，請參閱 NOTES 區段以自訂屬性及建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f3d52-117">Specifies the properties used to describe the customization steps of the image, like Image source etc. To construct, see NOTES section for CUSTOMIZE properties and create a hash table.</span></span>

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

### <span data-ttu-id="f3d52-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3d52-118">-DefaultProfile</span></span>
<span data-ttu-id="f3d52-119">Region HideParameter 用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f3d52-119">region HideParameter The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3d52-120">-發佈</span><span class="sxs-lookup"><span data-stu-id="f3d52-120">-Distribute</span></span>
<span data-ttu-id="f3d52-121">此分配會針對影像輸出需要前往的地方進行。</span><span class="sxs-lookup"><span data-stu-id="f3d52-121">The distribution targets where the image output needs to go to.</span></span>
<span data-ttu-id="f3d52-122">若要建構，請參閱 DISTRIBUTE 屬性的附注區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f3d52-122">To construct, see NOTES section for DISTRIBUTE properties and create a hash table.</span></span>

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

### <span data-ttu-id="f3d52-123">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="f3d52-123">-ImageTemplateName</span></span>
<span data-ttu-id="f3d52-124">圖像範本的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3d52-124">The name of the image Template.</span></span>

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

### <span data-ttu-id="f3d52-125">-LastRunStatusEndTime</span><span class="sxs-lookup"><span data-stu-id="f3d52-125">-LastRunStatusEndTime</span></span>
<span data-ttu-id="f3d52-126">最後一次執行結束時間 (UTC) 。</span><span class="sxs-lookup"><span data-stu-id="f3d52-126">End time of the last run (UTC).</span></span>

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

### <span data-ttu-id="f3d52-127">-LastRunStatusMessage</span><span class="sxs-lookup"><span data-stu-id="f3d52-127">-LastRunStatusMessage</span></span>
<span data-ttu-id="f3d52-128">上次執行狀態詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="f3d52-128">Verbose information about the last run state.</span></span>

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

### <span data-ttu-id="f3d52-129">-LastRunStatusRunState</span><span class="sxs-lookup"><span data-stu-id="f3d52-129">-LastRunStatusRunState</span></span>
<span data-ttu-id="f3d52-130">上次執行的狀態。</span><span class="sxs-lookup"><span data-stu-id="f3d52-130">State of the last run.</span></span>

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

### <span data-ttu-id="f3d52-131">-LastRunStatusRunSubState</span><span class="sxs-lookup"><span data-stu-id="f3d52-131">-LastRunStatusRunSubState</span></span>
<span data-ttu-id="f3d52-132">上次執行之子狀態。</span><span class="sxs-lookup"><span data-stu-id="f3d52-132">Sub-state of the last run.</span></span>

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

### <span data-ttu-id="f3d52-133">-LastRunStatusStartTime</span><span class="sxs-lookup"><span data-stu-id="f3d52-133">-LastRunStatusStartTime</span></span>
<span data-ttu-id="f3d52-134">最後一次執行的時間 (UTC) 。</span><span class="sxs-lookup"><span data-stu-id="f3d52-134">Start time of the last run (UTC).</span></span>

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

### <span data-ttu-id="f3d52-135">-位置</span><span class="sxs-lookup"><span data-stu-id="f3d52-135">-Location</span></span>
<span data-ttu-id="f3d52-136">資源位置。</span><span class="sxs-lookup"><span data-stu-id="f3d52-136">Resource location.</span></span>

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

### <span data-ttu-id="f3d52-137">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f3d52-137">-NoWait</span></span>
<span data-ttu-id="f3d52-138">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="f3d52-138">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f3d52-139">-ProvisioningErrorCode</span><span class="sxs-lookup"><span data-stu-id="f3d52-139">-ProvisioningErrorCode</span></span>
<span data-ttu-id="f3d52-140">提供失敗的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f3d52-140">Error code of the provisioning failure.</span></span>

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

### <span data-ttu-id="f3d52-141">-ProvisioningErrorMessage</span><span class="sxs-lookup"><span data-stu-id="f3d52-141">-ProvisioningErrorMessage</span></span>
<span data-ttu-id="f3d52-142">布備失敗的詳細資訊錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="f3d52-142">Verbose error message about the provisioning failure.</span></span>

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

### <span data-ttu-id="f3d52-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3d52-143">-ResourceGroupName</span></span>
<span data-ttu-id="f3d52-144">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3d52-144">The name of the resource group.</span></span>

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

### <span data-ttu-id="f3d52-145">-來源</span><span class="sxs-lookup"><span data-stu-id="f3d52-145">-Source</span></span>
<span data-ttu-id="f3d52-146">說明建立、自訂及散發的虛擬機器映射來源。</span><span class="sxs-lookup"><span data-stu-id="f3d52-146">Describes a virtual machine image source for building, customizing and distributing.</span></span>
<span data-ttu-id="f3d52-147">若要建構，請參閱 SOURCE 屬性的附注區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f3d52-147">To construct, see NOTES section for SOURCE properties and create a hash table.</span></span>

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

### <span data-ttu-id="f3d52-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f3d52-148">-SubscriptionId</span></span>
<span data-ttu-id="f3d52-149">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="f3d52-149">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>

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

### <span data-ttu-id="f3d52-150">-標記</span><span class="sxs-lookup"><span data-stu-id="f3d52-150">-Tag</span></span>
<span data-ttu-id="f3d52-151">資源標記。</span><span class="sxs-lookup"><span data-stu-id="f3d52-151">Resource tags.</span></span>

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

### <span data-ttu-id="f3d52-152">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="f3d52-152">-UserAssignedIdentityId</span></span>
<span data-ttu-id="f3d52-153">使用者指派身分識別的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f3d52-153">The id of user assigned identity.</span></span>

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

### <span data-ttu-id="f3d52-154">-VMProfileOscioSizeInGb</span><span class="sxs-lookup"><span data-stu-id="f3d52-154">-VMProfileOsdiskSizeInGb</span></span>
<span data-ttu-id="f3d52-155">作業系統磁片的大小 ，以 GB 為單位。</span><span class="sxs-lookup"><span data-stu-id="f3d52-155">Size of the OS disk in GB.</span></span>
<span data-ttu-id="f3d52-156">省略或指定 0 以使用 Azure 的預設作業系統磁片大小。</span><span class="sxs-lookup"><span data-stu-id="f3d52-156">Omit or specify 0 to use Azure's default OS disk size.</span></span>

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

### <span data-ttu-id="f3d52-157">-VMProfile VmSize</span><span class="sxs-lookup"><span data-stu-id="f3d52-157">-VMProfileVmSize</span></span>
<span data-ttu-id="f3d52-158">用來建立、自訂及捕獲影像的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="f3d52-158">Size of the virtual machine used to build, customize and capture images.</span></span>
<span data-ttu-id="f3d52-159">省略或指定空字串以使用預設 (Standard_D1_v2) 。</span><span class="sxs-lookup"><span data-stu-id="f3d52-159">Omit or specify empty string to use the default (Standard_D1_v2).</span></span>

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

### <span data-ttu-id="f3d52-160">-VnetConfigSubnetId</span><span class="sxs-lookup"><span data-stu-id="f3d52-160">-VnetConfigSubnetId</span></span>
<span data-ttu-id="f3d52-161">預先存在子網的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f3d52-161">Resource id of a pre-existing subnet.</span></span>

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

### <span data-ttu-id="f3d52-162">-確認</span><span class="sxs-lookup"><span data-stu-id="f3d52-162">-Confirm</span></span>
<span data-ttu-id="f3d52-163">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f3d52-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3d52-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3d52-164">-WhatIf</span></span>
<span data-ttu-id="f3d52-165">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f3d52-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3d52-166">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f3d52-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3d52-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3d52-167">CommonParameters</span></span>
<span data-ttu-id="f3d52-168">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f3d52-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3d52-169">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f3d52-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3d52-170">輸入</span><span class="sxs-lookup"><span data-stu-id="f3d52-170">INPUTS</span></span>

## <span data-ttu-id="f3d52-171">輸出</span><span class="sxs-lookup"><span data-stu-id="f3d52-171">OUTPUTS</span></span>

### <span data-ttu-id="f3d52-172">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span><span class="sxs-lookup"><span data-stu-id="f3d52-172">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span></span>

## <span data-ttu-id="f3d52-173">筆記</span><span class="sxs-lookup"><span data-stu-id="f3d52-173">NOTES</span></span>

<span data-ttu-id="f3d52-174">別名</span><span class="sxs-lookup"><span data-stu-id="f3d52-174">ALIASES</span></span>

<span data-ttu-id="f3d52-175">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="f3d52-175">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f3d52-176">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f3d52-176">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f3d52-177">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="f3d52-177">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f3d52-178">自訂<IImageTemplateCustomizer[]>：指定用來描述影像自訂步驟的屬性，例如圖像來源等。</span><span class="sxs-lookup"><span data-stu-id="f3d52-178">CUSTOMIZE <IImageTemplateCustomizer[]>: Specifies the properties used to describe the customization steps of the image, like Image source etc.</span></span>
  - <span data-ttu-id="f3d52-179">`Type <String>`：您想要在影像上使用的自訂工具類型。</span><span class="sxs-lookup"><span data-stu-id="f3d52-179">`Type <String>`: The type of customization tool you want to use on the Image.</span></span> <span data-ttu-id="f3d52-180">例如，"Shell" 可以是 shell 自訂程式</span><span class="sxs-lookup"><span data-stu-id="f3d52-180">For example, "Shell" can be shell customizer</span></span>
  - <span data-ttu-id="f3d52-181">`[Name <String>]`：好用名稱，提供此自訂步驟功能相關內容</span><span class="sxs-lookup"><span data-stu-id="f3d52-181">`[Name <String>]`: Friendly Name to provide context on what this customization step does</span></span>

<span data-ttu-id="f3d52-182">DISTRIBUTE <IImageTemplateDistributor[]>：此分配會檢查影像輸出必須前往的目標位置。</span><span class="sxs-lookup"><span data-stu-id="f3d52-182">DISTRIBUTE <IImageTemplateDistributor[]>: The distribution targets where the image output needs to go to.</span></span>
  - <span data-ttu-id="f3d52-183">`RunOutputName <String>`：用於相關聯 RunOutput 的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3d52-183">`RunOutputName <String>`: The name to be used for the associated RunOutput.</span></span>
  - <span data-ttu-id="f3d52-184">`Type <String>`：分配類型。</span><span class="sxs-lookup"><span data-stu-id="f3d52-184">`Type <String>`: Type of distribution.</span></span>
  - <span data-ttu-id="f3d52-185">`[ArtifactTag <IImageTemplateDistributorArtifactTags>]`：發行者建立/更新產品後，將會用於其上的標記。</span><span class="sxs-lookup"><span data-stu-id="f3d52-185">`[ArtifactTag <IImageTemplateDistributorArtifactTags>]`: Tags that will be applied to the artifact once it has been created/updated by the distributor.</span></span>
    - <span data-ttu-id="f3d52-186">`[(Any) <String>]`：這表示任何屬性都可以新增到這個物件。</span><span class="sxs-lookup"><span data-stu-id="f3d52-186">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

<span data-ttu-id="f3d52-187">來源 <IImageTemplateSource> ：說明建立、自訂及散發的虛擬機器映射來源。</span><span class="sxs-lookup"><span data-stu-id="f3d52-187">SOURCE <IImageTemplateSource>: Describes a virtual machine image source for building, customizing and distributing.</span></span>
  - <span data-ttu-id="f3d52-188">`Type <String>`：指定您想要開始的來源影像類型。</span><span class="sxs-lookup"><span data-stu-id="f3d52-188">`Type <String>`: Specifies the type of source image you want to start with.</span></span>

## <span data-ttu-id="f3d52-189">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3d52-189">RELATED LINKS</span></span>

