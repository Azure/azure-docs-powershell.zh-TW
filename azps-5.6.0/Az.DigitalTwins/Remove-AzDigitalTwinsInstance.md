---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/remove-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsInstance.md
ms.openlocfilehash: ff83b10755789f807e1ec28b1f247c9ebee1da18
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910173"
---
# <span data-ttu-id="8f13b-101">Remove-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="8f13b-101">Remove-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="8f13b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8f13b-102">SYNOPSIS</span></span>
<span data-ttu-id="8f13b-103">刪除 DigitalTwinsInstance。</span><span class="sxs-lookup"><span data-stu-id="8f13b-103">Delete a DigitalTwinsInstance.</span></span>

## <span data-ttu-id="8f13b-104">語法</span><span class="sxs-lookup"><span data-stu-id="8f13b-104">SYNTAX</span></span>

### <span data-ttu-id="8f13b-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="8f13b-105">Delete (Default)</span></span>
```
Remove-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8f13b-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8f13b-106">DeleteViaIdentity</span></span>
```
Remove-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8f13b-107">描述</span><span class="sxs-lookup"><span data-stu-id="8f13b-107">DESCRIPTION</span></span>
<span data-ttu-id="8f13b-108">刪除 DigitalTwinsInstance。</span><span class="sxs-lookup"><span data-stu-id="8f13b-108">Delete a DigitalTwinsInstance.</span></span>

## <span data-ttu-id="8f13b-109">例子</span><span class="sxs-lookup"><span data-stu-id="8f13b-109">EXAMPLES</span></span>

### <span data-ttu-id="8f13b-110">範例 1：移除 AzDigitalTwinsInstance by name</span><span class="sxs-lookup"><span data-stu-id="8f13b-110">Example 1: Remove an AzDigitalTwinsInstance by name</span></span>
```powershell
PS C:\> Remove-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin


```

<span data-ttu-id="8f13b-111">此命令會移除 AzDigitalTwinsInstance 的名稱</span><span class="sxs-lookup"><span data-stu-id="8f13b-111">This command removes an AzDigitalTwinsInstance by name</span></span>

### <span data-ttu-id="8f13b-112">範例 2：移除 AzDigitalTwinsInstance by InputObject</span><span class="sxs-lookup"><span data-stu-id="8f13b-112">Example 2: Remove an AzDigitalTwinsInstance by InputObject</span></span>
```powershell
PS C:\> $GetAzDigitalTwins =  Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Remove-AzDigitalTwinsInstance -InputObject $GetAzDigitalTwins


```

<span data-ttu-id="8f13b-113">此命令會移除 AzDigitalTwinsInstance 的名稱</span><span class="sxs-lookup"><span data-stu-id="8f13b-113">This command removes an AzDigitalTwinsInstance by name</span></span>

## <span data-ttu-id="8f13b-114">參數</span><span class="sxs-lookup"><span data-stu-id="8f13b-114">PARAMETERS</span></span>

### <span data-ttu-id="8f13b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f13b-115">-AsJob</span></span>
<span data-ttu-id="8f13b-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="8f13b-116">Run the command as a job</span></span>

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

### <span data-ttu-id="8f13b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f13b-117">-DefaultProfile</span></span>
<span data-ttu-id="8f13b-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8f13b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f13b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f13b-119">-InputObject</span></span>
<span data-ttu-id="8f13b-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8f13b-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8f13b-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8f13b-121">-NoWait</span></span>
<span data-ttu-id="8f13b-122">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="8f13b-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8f13b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f13b-123">-PassThru</span></span>
<span data-ttu-id="8f13b-124">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="8f13b-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8f13b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f13b-125">-ResourceGroupName</span></span>
<span data-ttu-id="8f13b-126">包含 DigitalTwinsInstance 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="8f13b-126">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="8f13b-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="8f13b-127">-ResourceName</span></span>
<span data-ttu-id="8f13b-128">DigitalTwinsInstance 的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f13b-128">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="8f13b-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8f13b-129">-SubscriptionId</span></span>
<span data-ttu-id="8f13b-130">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="8f13b-130">The subscription identifier.</span></span>

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

### <span data-ttu-id="8f13b-131">-確認</span><span class="sxs-lookup"><span data-stu-id="8f13b-131">-Confirm</span></span>
<span data-ttu-id="8f13b-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8f13b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f13b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f13b-133">-WhatIf</span></span>
<span data-ttu-id="8f13b-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8f13b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f13b-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8f13b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f13b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f13b-136">CommonParameters</span></span>
<span data-ttu-id="8f13b-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8f13b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f13b-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f13b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f13b-139">輸入</span><span class="sxs-lookup"><span data-stu-id="8f13b-139">INPUTS</span></span>

### <span data-ttu-id="8f13b-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="8f13b-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="8f13b-141">輸出</span><span class="sxs-lookup"><span data-stu-id="8f13b-141">OUTPUTS</span></span>

### <span data-ttu-id="8f13b-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="8f13b-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="8f13b-143">筆記</span><span class="sxs-lookup"><span data-stu-id="8f13b-143">NOTES</span></span>

<span data-ttu-id="8f13b-144">別名</span><span class="sxs-lookup"><span data-stu-id="8f13b-144">ALIASES</span></span>

<span data-ttu-id="8f13b-145">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="8f13b-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8f13b-146">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8f13b-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8f13b-147">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="8f13b-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8f13b-148">INPUTOBJECT： <IDigitalTwinsIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="8f13b-148">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8f13b-149">`[EndpointName <String>]`：端點資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f13b-149">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="8f13b-150">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="8f13b-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8f13b-151">`[Location <String>]`：DigitalTwinsInstance 的位置。</span><span class="sxs-lookup"><span data-stu-id="8f13b-151">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="8f13b-152">`[ResourceGroupName <String>]`：包含 DigitalTwinsInstance 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="8f13b-152">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="8f13b-153">`[ResourceName <String>]`：DigitalTwinsInstance 的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f13b-153">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="8f13b-154">`[SubscriptionId <String>]`：訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="8f13b-154">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="8f13b-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="8f13b-155">RELATED LINKS</span></span>

