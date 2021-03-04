---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/test-azdigitaltwinsinstancenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Test-AzDigitalTwinsInstanceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Test-AzDigitalTwinsInstanceNameAvailability.md
ms.openlocfilehash: d33f092bc72f480766ed81de66abbe1e001dfa42
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910170"
---
# <span data-ttu-id="d79af-101">Test-AzDigitalTwinsInstanceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="d79af-101">Test-AzDigitalTwinsInstanceNameAvailability</span></span>

## <span data-ttu-id="d79af-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d79af-102">SYNOPSIS</span></span>
<span data-ttu-id="d79af-103">檢查是否提供 DigitalTwinsInstance 名稱。</span><span class="sxs-lookup"><span data-stu-id="d79af-103">Check if a DigitalTwinsInstance name is available.</span></span>

## <span data-ttu-id="d79af-104">語法</span><span class="sxs-lookup"><span data-stu-id="d79af-104">SYNTAX</span></span>

### <span data-ttu-id="d79af-105">CheckExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="d79af-105">CheckExpanded (Default)</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -Location <String> -Name <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d79af-106">檢查</span><span class="sxs-lookup"><span data-stu-id="d79af-106">Check</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -Location <String>
 -DigitalTwinsInstanceCheckName <ICheckNameRequest> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d79af-107">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d79af-107">CheckViaIdentity</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -InputObject <IDigitalTwinsIdentity>
 -DigitalTwinsInstanceCheckName <ICheckNameRequest> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="d79af-108">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d79af-108">CheckViaIdentityExpanded</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -InputObject <IDigitalTwinsIdentity> -Name <String>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d79af-109">描述</span><span class="sxs-lookup"><span data-stu-id="d79af-109">DESCRIPTION</span></span>
<span data-ttu-id="d79af-110">檢查是否提供 DigitalTwinsInstance 名稱。</span><span class="sxs-lookup"><span data-stu-id="d79af-110">Check if a DigitalTwinsInstance name is available.</span></span>

## <span data-ttu-id="d79af-111">例子</span><span class="sxs-lookup"><span data-stu-id="d79af-111">EXAMPLES</span></span>

### <span data-ttu-id="d79af-112">範例 1：根據位置和名稱檢查名稱。</span><span class="sxs-lookup"><span data-stu-id="d79af-112">Example 1: Check the name by location and name.</span></span>
```powershell
PS C:\> Test-AzDigitalTwinsInstanceNameAvailability -Location eastus -name youriTestName

Message                       NameAvailable Reason
-------                       ------------- ------
'youriTestName' is available. True
```

<span data-ttu-id="d79af-113">根據位置和名稱檢查名稱的可用性。</span><span class="sxs-lookup"><span data-stu-id="d79af-113">Check the availability of the name by location and name.</span></span>

### <span data-ttu-id="d79af-114">範例 2：使用 DigitalTwinsObject 和 CheckNameObject 檢查名稱。</span><span class="sxs-lookup"><span data-stu-id="d79af-114">Example 2: Check the name by DigitalTwinsObject and CheckNameObject.</span></span>
```powershell
PS C:\> $getAzDT =Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest 
$checkName = New-AzDigitalTwinsCheckNameRequestObject -name youriTestName
Test-AzDigitalTwinsInstanceNameAvailability -InputObject $getAzDT -DigitalTwinsInstanceCheckName $checkName

Message                     NameAvailable Reason
-------                     ------------- ------
'youriTestName' is available. True
```

<span data-ttu-id="d79af-115">取得 DigitalTwinsInstance，然後建立一個 Requset 物件來測試名稱的可用性。</span><span class="sxs-lookup"><span data-stu-id="d79af-115">Get A DigitalTwinsInstance and create a Requset Object to Test the availability of the name.</span></span>

## <span data-ttu-id="d79af-116">參數</span><span class="sxs-lookup"><span data-stu-id="d79af-116">PARAMETERS</span></span>

### <span data-ttu-id="d79af-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d79af-117">-DefaultProfile</span></span>
<span data-ttu-id="d79af-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d79af-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d79af-119">-DigitalTwinsInstanceCheckName</span><span class="sxs-lookup"><span data-stu-id="d79af-119">-DigitalTwinsInstanceCheckName</span></span>
<span data-ttu-id="d79af-120">從資料庫檢查名稱可用性要求所返回的結果。</span><span class="sxs-lookup"><span data-stu-id="d79af-120">The result returned from a database check name availability request.</span></span>
<span data-ttu-id="d79af-121">若要建構，請參閱 DIGITALTWINSINSTANCECHECKNAME 屬性的附注區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="d79af-121">To construct, see NOTES section for DIGITALTWINSINSTANCECHECKNAME properties and create a hash table.</span></span>

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

### <span data-ttu-id="d79af-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d79af-122">-InputObject</span></span>
<span data-ttu-id="d79af-123">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="d79af-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d79af-124">-位置</span><span class="sxs-lookup"><span data-stu-id="d79af-124">-Location</span></span>
<span data-ttu-id="d79af-125">DigitalTwinsInstance 的位置。</span><span class="sxs-lookup"><span data-stu-id="d79af-125">Location of DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="d79af-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="d79af-126">-Name</span></span>
<span data-ttu-id="d79af-127">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="d79af-127">Resource name.</span></span>

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

### <span data-ttu-id="d79af-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d79af-128">-SubscriptionId</span></span>
<span data-ttu-id="d79af-129">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="d79af-129">The subscription identifier.</span></span>

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

### <span data-ttu-id="d79af-130">-確認</span><span class="sxs-lookup"><span data-stu-id="d79af-130">-Confirm</span></span>
<span data-ttu-id="d79af-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d79af-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d79af-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d79af-132">-WhatIf</span></span>
<span data-ttu-id="d79af-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d79af-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d79af-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d79af-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d79af-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d79af-135">CommonParameters</span></span>
<span data-ttu-id="d79af-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d79af-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d79af-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d79af-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d79af-138">輸入</span><span class="sxs-lookup"><span data-stu-id="d79af-138">INPUTS</span></span>

### <span data-ttu-id="d79af-139">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameRequest</span><span class="sxs-lookup"><span data-stu-id="d79af-139">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameRequest</span></span>

### <span data-ttu-id="d79af-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="d79af-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="d79af-141">輸出</span><span class="sxs-lookup"><span data-stu-id="d79af-141">OUTPUTS</span></span>

### <span data-ttu-id="d79af-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.models.Api20201031.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="d79af-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameResult</span></span>

## <span data-ttu-id="d79af-143">筆記</span><span class="sxs-lookup"><span data-stu-id="d79af-143">NOTES</span></span>

<span data-ttu-id="d79af-144">別名</span><span class="sxs-lookup"><span data-stu-id="d79af-144">ALIASES</span></span>

<span data-ttu-id="d79af-145">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="d79af-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d79af-146">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="d79af-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d79af-147">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="d79af-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d79af-148">DIGITALTWINSINSTANCECHECKNAME：從資料庫檢查名稱可用性 <ICheckNameRequest> 要求傳回的結果。</span><span class="sxs-lookup"><span data-stu-id="d79af-148">DIGITALTWINSINSTANCECHECKNAME <ICheckNameRequest>: The result returned from a database check name availability request.</span></span>
  - <span data-ttu-id="d79af-149">`Name <String>`：資源名稱。</span><span class="sxs-lookup"><span data-stu-id="d79af-149">`Name <String>`: Resource name.</span></span>

<span data-ttu-id="d79af-150">INPUTOBJECT： <IDigitalTwinsIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="d79af-150">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d79af-151">`[EndpointName <String>]`：端點資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="d79af-151">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="d79af-152">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="d79af-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d79af-153">`[Location <String>]`：DigitalTwinsInstance 的位置。</span><span class="sxs-lookup"><span data-stu-id="d79af-153">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="d79af-154">`[ResourceGroupName <String>]`：包含 DigitalTwinsInstance 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="d79af-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="d79af-155">`[ResourceName <String>]`：DigitalTwinsInstance 的名稱。</span><span class="sxs-lookup"><span data-stu-id="d79af-155">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="d79af-156">`[SubscriptionId <String>]`：訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="d79af-156">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="d79af-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="d79af-157">RELATED LINKS</span></span>

