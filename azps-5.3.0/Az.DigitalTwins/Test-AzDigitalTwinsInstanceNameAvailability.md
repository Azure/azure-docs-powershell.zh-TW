---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/test-azdigitaltwinsinstancenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Test-AzDigitalTwinsInstanceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Test-AzDigitalTwinsInstanceNameAvailability.md
ms.openlocfilehash: af911fc4eb4cccbd3f22e0d54a8aad2933b5db46
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435184"
---
# <span data-ttu-id="e24ee-101">Test-AzDigitalTwinsInstanceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="e24ee-101">Test-AzDigitalTwinsInstanceNameAvailability</span></span>

## <span data-ttu-id="e24ee-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e24ee-102">SYNOPSIS</span></span>
<span data-ttu-id="e24ee-103">檢查是否有可用的 DigitalTwinsInstance 名稱。</span><span class="sxs-lookup"><span data-stu-id="e24ee-103">Check if a DigitalTwinsInstance name is available.</span></span>

## <span data-ttu-id="e24ee-104">句法</span><span class="sxs-lookup"><span data-stu-id="e24ee-104">SYNTAX</span></span>

### <span data-ttu-id="e24ee-105">CheckExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="e24ee-105">CheckExpanded (Default)</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -Location <String> -Name <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e24ee-106">確認</span><span class="sxs-lookup"><span data-stu-id="e24ee-106">Check</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -Location <String>
 -DigitalTwinsInstanceCheckName <ICheckNameRequest> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e24ee-107">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e24ee-107">CheckViaIdentity</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -InputObject <IDigitalTwinsIdentity>
 -DigitalTwinsInstanceCheckName <ICheckNameRequest> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="e24ee-108">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e24ee-108">CheckViaIdentityExpanded</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -InputObject <IDigitalTwinsIdentity> -Name <String>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e24ee-109">說明</span><span class="sxs-lookup"><span data-stu-id="e24ee-109">DESCRIPTION</span></span>
<span data-ttu-id="e24ee-110">檢查是否有可用的 DigitalTwinsInstance 名稱。</span><span class="sxs-lookup"><span data-stu-id="e24ee-110">Check if a DigitalTwinsInstance name is available.</span></span>

## <span data-ttu-id="e24ee-111">示例</span><span class="sxs-lookup"><span data-stu-id="e24ee-111">EXAMPLES</span></span>

### <span data-ttu-id="e24ee-112">範例1：依位置和名稱檢查名稱。</span><span class="sxs-lookup"><span data-stu-id="e24ee-112">Example 1: Check the name by location and name.</span></span>
```powershell
PS C:\> Test-AzDigitalTwinsInstanceNameAvailability -Location eastus -name youriTestName

Message                       NameAvailable Reason
-------                       ------------- ------
'youriTestName' is available. True
```

<span data-ttu-id="e24ee-113">依位置和名稱檢查名稱的可用性。</span><span class="sxs-lookup"><span data-stu-id="e24ee-113">Check the availability of the name by location and name.</span></span>

### <span data-ttu-id="e24ee-114">範例2：依 DigitalTwinsObject 和 CheckNameObject 檢查名稱。</span><span class="sxs-lookup"><span data-stu-id="e24ee-114">Example 2: Check the name by DigitalTwinsObject and CheckNameObject.</span></span>
```powershell
PS C:\> $getAzDT =Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest 
$checkName = New-AzDigitalTwinsCheckNameRequestObject -name youriTestName
Test-AzDigitalTwinsInstanceNameAvailability -InputObject $getAzDT -DigitalTwinsInstanceCheckName $checkName

Message                     NameAvailable Reason
-------                     ------------- ------
'youriTestName' is available. True
```

<span data-ttu-id="e24ee-115">取得 DigitalTwinsInstance 並建立 Requset 物件，以測試名稱的可用性。</span><span class="sxs-lookup"><span data-stu-id="e24ee-115">Get A DigitalTwinsInstance and create a Requset Object to Test the availability of the name.</span></span>

## <span data-ttu-id="e24ee-116">參數</span><span class="sxs-lookup"><span data-stu-id="e24ee-116">PARAMETERS</span></span>

### <span data-ttu-id="e24ee-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e24ee-117">-DefaultProfile</span></span>
<span data-ttu-id="e24ee-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e24ee-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e24ee-119">-DigitalTwinsInstanceCheckName</span><span class="sxs-lookup"><span data-stu-id="e24ee-119">-DigitalTwinsInstanceCheckName</span></span>
<span data-ttu-id="e24ee-120">從資料庫檢查名稱可用性要求傳回的結果。</span><span class="sxs-lookup"><span data-stu-id="e24ee-120">The result returned from a database check name availability request.</span></span>
<span data-ttu-id="e24ee-121">若要建立，請參閱 DIGITALTWINSINSTANCECHECKNAME 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="e24ee-121">To construct, see NOTES section for DIGITALTWINSINSTANCECHECKNAME properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameRequest
Parameter Sets: Check, CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e24ee-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e24ee-122">-InputObject</span></span>
<span data-ttu-id="e24ee-123">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e24ee-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: CheckViaIdentity, CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e24ee-124">-位置</span><span class="sxs-lookup"><span data-stu-id="e24ee-124">-Location</span></span>
<span data-ttu-id="e24ee-125">DigitalTwinsInstance 的位置。</span><span class="sxs-lookup"><span data-stu-id="e24ee-125">Location of DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Check, CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e24ee-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="e24ee-126">-Name</span></span>
<span data-ttu-id="e24ee-127">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="e24ee-127">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded, CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e24ee-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e24ee-128">-SubscriptionId</span></span>
<span data-ttu-id="e24ee-129">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="e24ee-129">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Check, CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e24ee-130">-確認</span><span class="sxs-lookup"><span data-stu-id="e24ee-130">-Confirm</span></span>
<span data-ttu-id="e24ee-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e24ee-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e24ee-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e24ee-132">-WhatIf</span></span>
<span data-ttu-id="e24ee-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e24ee-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e24ee-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e24ee-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e24ee-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e24ee-135">CommonParameters</span></span>
<span data-ttu-id="e24ee-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e24ee-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e24ee-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e24ee-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e24ee-138">輸入</span><span class="sxs-lookup"><span data-stu-id="e24ee-138">INPUTS</span></span>

### <span data-ttu-id="e24ee-139">ICheckNameRequest （DigitalTwins）。 Api20201031。</span><span class="sxs-lookup"><span data-stu-id="e24ee-139">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameRequest</span></span>

### <span data-ttu-id="e24ee-140">IDigitalTwinsIdentity （DigitalTwins）的</span><span class="sxs-lookup"><span data-stu-id="e24ee-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="e24ee-141">輸出</span><span class="sxs-lookup"><span data-stu-id="e24ee-141">OUTPUTS</span></span>

### <span data-ttu-id="e24ee-142">ICheckNameResult （DigitalTwins）。 Api20201031。</span><span class="sxs-lookup"><span data-stu-id="e24ee-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameResult</span></span>

## <span data-ttu-id="e24ee-143">筆記</span><span class="sxs-lookup"><span data-stu-id="e24ee-143">NOTES</span></span>

<span data-ttu-id="e24ee-144">別名</span><span class="sxs-lookup"><span data-stu-id="e24ee-144">ALIASES</span></span>

<span data-ttu-id="e24ee-145">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="e24ee-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e24ee-146">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="e24ee-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e24ee-147">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="e24ee-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e24ee-148">DIGITALTWINSINSTANCECHECKNAME <ICheckNameRequest> ：從資料庫檢查名稱可用性要求傳回的結果。</span><span class="sxs-lookup"><span data-stu-id="e24ee-148">DIGITALTWINSINSTANCECHECKNAME <ICheckNameRequest>: The result returned from a database check name availability request.</span></span>
  - <span data-ttu-id="e24ee-149">`Name <String>`：資源名稱。</span><span class="sxs-lookup"><span data-stu-id="e24ee-149">`Name <String>`: Resource name.</span></span>

<span data-ttu-id="e24ee-150">INPUTOBJECT <IDigitalTwinsIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="e24ee-150">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e24ee-151">`[EndpointName <String>]`：端點資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="e24ee-151">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="e24ee-152">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="e24ee-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e24ee-153">`[Location <String>]`： DigitalTwinsInstance 的位置。</span><span class="sxs-lookup"><span data-stu-id="e24ee-153">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="e24ee-154">`[ResourceGroupName <String>]`：包含 DigitalTwinsInstance 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e24ee-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="e24ee-155">`[ResourceName <String>]`： DigitalTwinsInstance 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e24ee-155">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="e24ee-156">`[SubscriptionId <String>]`：訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="e24ee-156">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="e24ee-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="e24ee-157">RELATED LINKS</span></span>

