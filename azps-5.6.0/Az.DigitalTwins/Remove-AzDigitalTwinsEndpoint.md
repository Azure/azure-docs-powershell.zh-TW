---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/remove-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: f7d8b5665ff150e0501d77a76c2dde7e4a947cb5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910174"
---
# <span data-ttu-id="e85f9-101">Remove-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="e85f9-101">Remove-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="e85f9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e85f9-102">SYNOPSIS</span></span>
<span data-ttu-id="e85f9-103">刪除 DigitalTwinsInstance 端點。</span><span class="sxs-lookup"><span data-stu-id="e85f9-103">Delete a DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="e85f9-104">語法</span><span class="sxs-lookup"><span data-stu-id="e85f9-104">SYNTAX</span></span>

### <span data-ttu-id="e85f9-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="e85f9-105">Delete (Default)</span></span>
```
Remove-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="e85f9-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e85f9-106">DeleteViaIdentity</span></span>
```
Remove-AzDigitalTwinsEndpoint -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e85f9-107">描述</span><span class="sxs-lookup"><span data-stu-id="e85f9-107">DESCRIPTION</span></span>
<span data-ttu-id="e85f9-108">刪除 DigitalTwinsInstance 端點。</span><span class="sxs-lookup"><span data-stu-id="e85f9-108">Delete a DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="e85f9-109">例子</span><span class="sxs-lookup"><span data-stu-id="e85f9-109">EXAMPLES</span></span>

### <span data-ttu-id="e85f9-110">範例 1：刪除 EndPointName 的 azDigitalTwinsEndPoint</span><span class="sxs-lookup"><span data-stu-id="e85f9-110">Example 1: Delete the azDigitalTwinsEndPoint by EndPointName</span></span>
```powershell
PS C:\> Remove-AzDigitalTwinsEndpoint -ResourceGroupName youritemp -EndpointName youriEHEndpoint -ResourceName youriDigitalTwinsTest

```

<span data-ttu-id="e85f9-111">刪除 EndPointName ResourceGroupName 和 ResourceName 的 azDigitalTwinsEndPoint</span><span class="sxs-lookup"><span data-stu-id="e85f9-111">Delete the azDigitalTwinsEndPoint by EndPointName ResourceGroupName and ResourceName</span></span>

### <span data-ttu-id="e85f9-112">範例 2：刪除 azDigitalTwinsEndPoint by Object</span><span class="sxs-lookup"><span data-stu-id="e85f9-112">Example 2: Delete the azDigitalTwinsEndPoint by Object</span></span>
```powershell
PS C:\> $GetAzdigitalTwinsEndpoint = Get-AzDigitalTwinsEndpoint -EndpointName youriEHEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Remove-AzDigitalTwinsEndpoint -InputObject $GetAzdigitalTwinsEndpoint

```

<span data-ttu-id="e85f9-113">刪除 azDigitalTwinsEndPoint by Object</span><span class="sxs-lookup"><span data-stu-id="e85f9-113">Delete the azDigitalTwinsEndPoint by Object</span></span>

## <span data-ttu-id="e85f9-114">參數</span><span class="sxs-lookup"><span data-stu-id="e85f9-114">PARAMETERS</span></span>

### <span data-ttu-id="e85f9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e85f9-115">-AsJob</span></span>
<span data-ttu-id="e85f9-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="e85f9-116">Run the command as a job</span></span>

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

### <span data-ttu-id="e85f9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e85f9-117">-DefaultProfile</span></span>
<span data-ttu-id="e85f9-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e85f9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e85f9-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e85f9-119">-EndpointName</span></span>
<span data-ttu-id="e85f9-120">端點資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="e85f9-120">Name of Endpoint Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e85f9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e85f9-121">-InputObject</span></span>
<span data-ttu-id="e85f9-122">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e85f9-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e85f9-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e85f9-123">-NoWait</span></span>
<span data-ttu-id="e85f9-124">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="e85f9-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e85f9-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e85f9-125">-PassThru</span></span>
<span data-ttu-id="e85f9-126">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="e85f9-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e85f9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e85f9-127">-ResourceGroupName</span></span>
<span data-ttu-id="e85f9-128">包含 DigitalTwinsInstance 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="e85f9-128">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e85f9-129">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e85f9-129">-ResourceName</span></span>
<span data-ttu-id="e85f9-130">DigitalTwinsInstance 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e85f9-130">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e85f9-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e85f9-131">-SubscriptionId</span></span>
<span data-ttu-id="e85f9-132">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="e85f9-132">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e85f9-133">-確認</span><span class="sxs-lookup"><span data-stu-id="e85f9-133">-Confirm</span></span>
<span data-ttu-id="e85f9-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e85f9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e85f9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e85f9-135">-WhatIf</span></span>
<span data-ttu-id="e85f9-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e85f9-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e85f9-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e85f9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e85f9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e85f9-138">CommonParameters</span></span>
<span data-ttu-id="e85f9-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e85f9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e85f9-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e85f9-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e85f9-141">輸入</span><span class="sxs-lookup"><span data-stu-id="e85f9-141">INPUTS</span></span>

### <span data-ttu-id="e85f9-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="e85f9-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="e85f9-143">輸出</span><span class="sxs-lookup"><span data-stu-id="e85f9-143">OUTPUTS</span></span>

### <span data-ttu-id="e85f9-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="e85f9-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="e85f9-145">筆記</span><span class="sxs-lookup"><span data-stu-id="e85f9-145">NOTES</span></span>

<span data-ttu-id="e85f9-146">別名</span><span class="sxs-lookup"><span data-stu-id="e85f9-146">ALIASES</span></span>

<span data-ttu-id="e85f9-147">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="e85f9-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e85f9-148">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e85f9-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e85f9-149">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="e85f9-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e85f9-150">INPUTOBJECT： <IDigitalTwinsIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="e85f9-150">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e85f9-151">`[EndpointName <String>]`：端點資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="e85f9-151">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="e85f9-152">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="e85f9-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e85f9-153">`[Location <String>]`：DigitalTwinsInstance 的位置。</span><span class="sxs-lookup"><span data-stu-id="e85f9-153">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="e85f9-154">`[ResourceGroupName <String>]`：包含 DigitalTwinsInstance 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="e85f9-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="e85f9-155">`[ResourceName <String>]`：DigitalTwinsInstance 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e85f9-155">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="e85f9-156">`[SubscriptionId <String>]`：訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="e85f9-156">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="e85f9-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="e85f9-157">RELATED LINKS</span></span>

