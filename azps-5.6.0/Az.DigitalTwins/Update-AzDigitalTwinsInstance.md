---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/update-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Update-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Update-AzDigitalTwinsInstance.md
ms.openlocfilehash: 967b50b024e02d4a88fa2a1d91905acad5385b6d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910162"
---
# <span data-ttu-id="a363e-101">Update-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="a363e-101">Update-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="a363e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a363e-102">SYNOPSIS</span></span>
<span data-ttu-id="a363e-103">更新 DigitalTwinsInstance 的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="a363e-103">Update metadata of DigitalTwinsInstance.</span></span>

## <span data-ttu-id="a363e-104">語法</span><span class="sxs-lookup"><span data-stu-id="a363e-104">SYNTAX</span></span>

### <span data-ttu-id="a363e-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="a363e-105">UpdateExpanded (Default)</span></span>
```
Update-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a363e-106">更新</span><span class="sxs-lookup"><span data-stu-id="a363e-106">Update</span></span>
```
Update-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String>
 -DigitalTwinsPatchDescription <IDigitalTwinsPatchDescription> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a363e-107">UpdateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a363e-107">UpdateViaIdentity</span></span>
```
Update-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity>
 -DigitalTwinsPatchDescription <IDigitalTwinsPatchDescription> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a363e-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a363e-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a363e-109">描述</span><span class="sxs-lookup"><span data-stu-id="a363e-109">DESCRIPTION</span></span>
<span data-ttu-id="a363e-110">更新 DigitalTwinsInstance 的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="a363e-110">Update metadata of DigitalTwinsInstance.</span></span>

## <span data-ttu-id="a363e-111">例子</span><span class="sxs-lookup"><span data-stu-id="a363e-111">EXAMPLES</span></span>

### <span data-ttu-id="a363e-112">範例 1：UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="a363e-112">Example 1: UpdateExpanded (Default)</span></span>
```powershell
PS C:\> Update-AzDigitalTwinsInstance -ResourcegroupName youritemp -ResourceName youriDigitalTwinsTest -Tag @{“dtt”="001"}

Location Name                  Type
-------- ----                  ----
eastus   youriDigitalTwinsTest Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="a363e-113">更新 ResourceGroupName 指定的 DigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="a363e-113">Update the specified DigitalTwinsInstance by ResourceGroupName</span></span>

### <span data-ttu-id="a363e-114">範例 2：更新 AzDigitalTwinsInstance 由另一個 AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="a363e-114">Example 2: Update the AzDigitalTwinsInstance by another AzDigitalTwinsInstance</span></span>
```powershell
PS C:\> $updateDigitalTwinInstance1 = Update-AzDigitalTwinsInstance -ResourcegroupName youritemp -ResourceName youriDigitalTwin1 -Tag @{"dtt"="002"}
Update-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest -DigitalTwinsPatchDescription $updateDigitalTwinInstance1

Location Name                  Type
-------- ----                  ----
eastus   youriDigitalTwinsTest Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="a363e-115">由另一個 AzDigitalTwinsInstance 更新 AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="a363e-115">Update the AzDigitalTwinsInstance by another AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="a363e-116">參數</span><span class="sxs-lookup"><span data-stu-id="a363e-116">PARAMETERS</span></span>

### <span data-ttu-id="a363e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a363e-117">-DefaultProfile</span></span>
<span data-ttu-id="a363e-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a363e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a363e-119">-DigitalTwinsPatchDescription</span><span class="sxs-lookup"><span data-stu-id="a363e-119">-DigitalTwinsPatchDescription</span></span>
<span data-ttu-id="a363e-120">DigitalTwins 服務的描述。</span><span class="sxs-lookup"><span data-stu-id="a363e-120">The description of the DigitalTwins service.</span></span>
<span data-ttu-id="a363e-121">若要建構，請參閱 DIGITALTWINSPATCHDESCRIPTION 屬性的附注區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a363e-121">To construct, see NOTES section for DIGITALTWINSPATCHDESCRIPTION properties and create a hash table.</span></span>

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

### <span data-ttu-id="a363e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a363e-122">-InputObject</span></span>
<span data-ttu-id="a363e-123">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a363e-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a363e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a363e-124">-ResourceGroupName</span></span>
<span data-ttu-id="a363e-125">包含 DigitalTwinsInstance 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="a363e-125">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="a363e-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a363e-126">-ResourceName</span></span>
<span data-ttu-id="a363e-127">DigitalTwinsInstance 的名稱。</span><span class="sxs-lookup"><span data-stu-id="a363e-127">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="a363e-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a363e-128">-SubscriptionId</span></span>
<span data-ttu-id="a363e-129">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="a363e-129">The subscription identifier.</span></span>

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

### <span data-ttu-id="a363e-130">-標記</span><span class="sxs-lookup"><span data-stu-id="a363e-130">-Tag</span></span>
<span data-ttu-id="a363e-131">實例標記</span><span class="sxs-lookup"><span data-stu-id="a363e-131">Instance tags</span></span>

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

### <span data-ttu-id="a363e-132">-確認</span><span class="sxs-lookup"><span data-stu-id="a363e-132">-Confirm</span></span>
<span data-ttu-id="a363e-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a363e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a363e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a363e-134">-WhatIf</span></span>
<span data-ttu-id="a363e-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a363e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a363e-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a363e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a363e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a363e-137">CommonParameters</span></span>
<span data-ttu-id="a363e-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a363e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a363e-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a363e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a363e-140">輸入</span><span class="sxs-lookup"><span data-stu-id="a363e-140">INPUTS</span></span>

### <span data-ttu-id="a363e-141">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsPatchDescription</span><span class="sxs-lookup"><span data-stu-id="a363e-141">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsPatchDescription</span></span>

### <span data-ttu-id="a363e-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="a363e-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="a363e-143">輸出</span><span class="sxs-lookup"><span data-stu-id="a363e-143">OUTPUTS</span></span>

### <span data-ttu-id="a363e-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="a363e-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="a363e-145">筆記</span><span class="sxs-lookup"><span data-stu-id="a363e-145">NOTES</span></span>

<span data-ttu-id="a363e-146">別名</span><span class="sxs-lookup"><span data-stu-id="a363e-146">ALIASES</span></span>

<span data-ttu-id="a363e-147">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="a363e-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a363e-148">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a363e-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a363e-149">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="a363e-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a363e-150">DIGITALTWINSPATCHDESCRIPTION：DigitalTwins <IDigitalTwinsPatchDescription> 服務的描述。</span><span class="sxs-lookup"><span data-stu-id="a363e-150">DIGITALTWINSPATCHDESCRIPTION <IDigitalTwinsPatchDescription>: The description of the DigitalTwins service.</span></span>
  - <span data-ttu-id="a363e-151">`[Tag <IDigitalTwinsPatchDescriptionTags>]`：實例標記</span><span class="sxs-lookup"><span data-stu-id="a363e-151">`[Tag <IDigitalTwinsPatchDescriptionTags>]`: Instance tags</span></span>
    - <span data-ttu-id="a363e-152">`[(Any) <String>]`：這表示任何屬性都可以新增到這個物件。</span><span class="sxs-lookup"><span data-stu-id="a363e-152">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

<span data-ttu-id="a363e-153">INPUTOBJECT： <IDigitalTwinsIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="a363e-153">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a363e-154">`[EndpointName <String>]`：端點資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="a363e-154">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="a363e-155">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="a363e-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a363e-156">`[Location <String>]`：DigitalTwinsInstance 的位置。</span><span class="sxs-lookup"><span data-stu-id="a363e-156">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="a363e-157">`[ResourceGroupName <String>]`：包含 DigitalTwinsInstance 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="a363e-157">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="a363e-158">`[ResourceName <String>]`：DigitalTwinsInstance 的名稱。</span><span class="sxs-lookup"><span data-stu-id="a363e-158">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="a363e-159">`[SubscriptionId <String>]`：訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="a363e-159">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="a363e-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="a363e-160">RELATED LINKS</span></span>

