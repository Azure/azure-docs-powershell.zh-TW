---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/update-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Update-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Update-AzDigitalTwinsInstance.md
ms.openlocfilehash: 4de7ab82f60c651e23565569ccf2cda7f4d949b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436529"
---
# <span data-ttu-id="76225-101">Update-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="76225-101">Update-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="76225-102">摘要</span><span class="sxs-lookup"><span data-stu-id="76225-102">SYNOPSIS</span></span>
<span data-ttu-id="76225-103">更新 DigitalTwinsInstance 的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="76225-103">Update metadata of DigitalTwinsInstance.</span></span>

## <span data-ttu-id="76225-104">句法</span><span class="sxs-lookup"><span data-stu-id="76225-104">SYNTAX</span></span>

### <span data-ttu-id="76225-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="76225-105">UpdateExpanded (Default)</span></span>
```
Update-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="76225-106">時更新</span><span class="sxs-lookup"><span data-stu-id="76225-106">Update</span></span>
```
Update-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String>
 -DigitalTwinsPatchDescription <IDigitalTwinsPatchDescription> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="76225-107">UpdateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="76225-107">UpdateViaIdentity</span></span>
```
Update-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity>
 -DigitalTwinsPatchDescription <IDigitalTwinsPatchDescription> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="76225-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="76225-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="76225-109">說明</span><span class="sxs-lookup"><span data-stu-id="76225-109">DESCRIPTION</span></span>
<span data-ttu-id="76225-110">更新 DigitalTwinsInstance 的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="76225-110">Update metadata of DigitalTwinsInstance.</span></span>

## <span data-ttu-id="76225-111">示例</span><span class="sxs-lookup"><span data-stu-id="76225-111">EXAMPLES</span></span>

### <span data-ttu-id="76225-112">範例1： UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="76225-112">Example 1: UpdateExpanded (Default)</span></span>
```powershell
PS C:\> Update-AzDigitalTwinsInstance -ResourcegroupName youritemp -ResourceName youriDigitalTwinsTest -Tag @{“dtt”="001"}

Location Name                  Type
-------- ----                  ----
eastus   youriDigitalTwinsTest Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="76225-113">依 ResourceGroupName 更新指定的 DigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="76225-113">Update the specified DigitalTwinsInstance by ResourceGroupName</span></span>

### <span data-ttu-id="76225-114">範例2：由另一個 AzDigitalTwinsInstance 更新 AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="76225-114">Example 2: Update the AzDigitalTwinsInstance by another AzDigitalTwinsInstance</span></span>
```powershell
PS C:\> $updateDigitalTwinInstance1 = Update-AzDigitalTwinsInstance -ResourcegroupName youritemp -ResourceName youriDigitalTwin1 -Tag @{"dtt"="002"}
Update-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest -DigitalTwinsPatchDescription $updateDigitalTwinInstance1

Location Name                  Type
-------- ----                  ----
eastus   youriDigitalTwinsTest Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="76225-115">使用另一個 AzDigitalTwinsInstance 更新 AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="76225-115">Update the AzDigitalTwinsInstance by another AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="76225-116">參數</span><span class="sxs-lookup"><span data-stu-id="76225-116">PARAMETERS</span></span>

### <span data-ttu-id="76225-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76225-117">-DefaultProfile</span></span>
<span data-ttu-id="76225-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="76225-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76225-119">-DigitalTwinsPatchDescription</span><span class="sxs-lookup"><span data-stu-id="76225-119">-DigitalTwinsPatchDescription</span></span>
<span data-ttu-id="76225-120">DigitalTwins 服務的描述。</span><span class="sxs-lookup"><span data-stu-id="76225-120">The description of the DigitalTwins service.</span></span>
<span data-ttu-id="76225-121">若要建立，請參閱 DIGITALTWINSPATCHDESCRIPTION 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="76225-121">To construct, see NOTES section for DIGITALTWINSPATCHDESCRIPTION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsPatchDescription
Parameter Sets: Update, UpdateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76225-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76225-122">-InputObject</span></span>
<span data-ttu-id="76225-123">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="76225-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: UpdateViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76225-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76225-124">-ResourceGroupName</span></span>
<span data-ttu-id="76225-125">包含 DigitalTwinsInstance 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="76225-125">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76225-126">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="76225-126">-ResourceName</span></span>
<span data-ttu-id="76225-127">DigitalTwinsInstance 的名稱。</span><span class="sxs-lookup"><span data-stu-id="76225-127">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76225-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="76225-128">-SubscriptionId</span></span>
<span data-ttu-id="76225-129">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="76225-129">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76225-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="76225-130">-Tag</span></span>
<span data-ttu-id="76225-131">實例標記</span><span class="sxs-lookup"><span data-stu-id="76225-131">Instance tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76225-132">-確認</span><span class="sxs-lookup"><span data-stu-id="76225-132">-Confirm</span></span>
<span data-ttu-id="76225-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="76225-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76225-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76225-134">-WhatIf</span></span>
<span data-ttu-id="76225-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="76225-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76225-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="76225-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76225-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76225-137">CommonParameters</span></span>
<span data-ttu-id="76225-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="76225-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76225-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="76225-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76225-140">輸入</span><span class="sxs-lookup"><span data-stu-id="76225-140">INPUTS</span></span>

### <span data-ttu-id="76225-141">IDigitalTwinsPatchDescription （DigitalTwins）。 Api20201031。</span><span class="sxs-lookup"><span data-stu-id="76225-141">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsPatchDescription</span></span>

### <span data-ttu-id="76225-142">IDigitalTwinsIdentity （DigitalTwins）的</span><span class="sxs-lookup"><span data-stu-id="76225-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="76225-143">輸出</span><span class="sxs-lookup"><span data-stu-id="76225-143">OUTPUTS</span></span>

### <span data-ttu-id="76225-144">IDigitalTwinsDescription （DigitalTwins）。 Api20201031。</span><span class="sxs-lookup"><span data-stu-id="76225-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="76225-145">筆記</span><span class="sxs-lookup"><span data-stu-id="76225-145">NOTES</span></span>

<span data-ttu-id="76225-146">別名</span><span class="sxs-lookup"><span data-stu-id="76225-146">ALIASES</span></span>

<span data-ttu-id="76225-147">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="76225-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="76225-148">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="76225-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="76225-149">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="76225-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="76225-150">DIGITALTWINSPATCHDESCRIPTION <IDigitalTwinsPatchDescription> ： DigitalTwins 服務的描述。</span><span class="sxs-lookup"><span data-stu-id="76225-150">DIGITALTWINSPATCHDESCRIPTION <IDigitalTwinsPatchDescription>: The description of the DigitalTwins service.</span></span>
  - <span data-ttu-id="76225-151">`[Tag <IDigitalTwinsPatchDescriptionTags>]`：實例標記</span><span class="sxs-lookup"><span data-stu-id="76225-151">`[Tag <IDigitalTwinsPatchDescriptionTags>]`: Instance tags</span></span>
    - <span data-ttu-id="76225-152">`[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="76225-152">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

<span data-ttu-id="76225-153">INPUTOBJECT <IDigitalTwinsIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="76225-153">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="76225-154">`[EndpointName <String>]`：端點資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="76225-154">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="76225-155">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="76225-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="76225-156">`[Location <String>]`： DigitalTwinsInstance 的位置。</span><span class="sxs-lookup"><span data-stu-id="76225-156">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="76225-157">`[ResourceGroupName <String>]`：包含 DigitalTwinsInstance 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="76225-157">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="76225-158">`[ResourceName <String>]`： DigitalTwinsInstance 的名稱。</span><span class="sxs-lookup"><span data-stu-id="76225-158">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="76225-159">`[SubscriptionId <String>]`：訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="76225-159">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="76225-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="76225-160">RELATED LINKS</span></span>

