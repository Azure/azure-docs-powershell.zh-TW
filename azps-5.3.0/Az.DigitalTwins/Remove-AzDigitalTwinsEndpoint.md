---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/remove-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 1c740134cb2613a8efcd950fec4cd780f4f443cf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435186"
---
# <span data-ttu-id="50dea-101">Remove-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="50dea-101">Remove-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="50dea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="50dea-102">SYNOPSIS</span></span>
<span data-ttu-id="50dea-103">刪除 DigitalTwinsInstance 端點。</span><span class="sxs-lookup"><span data-stu-id="50dea-103">Delete a DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="50dea-104">句法</span><span class="sxs-lookup"><span data-stu-id="50dea-104">SYNTAX</span></span>

### <span data-ttu-id="50dea-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="50dea-105">Delete (Default)</span></span>
```
Remove-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="50dea-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="50dea-106">DeleteViaIdentity</span></span>
```
Remove-AzDigitalTwinsEndpoint -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="50dea-107">說明</span><span class="sxs-lookup"><span data-stu-id="50dea-107">DESCRIPTION</span></span>
<span data-ttu-id="50dea-108">刪除 DigitalTwinsInstance 端點。</span><span class="sxs-lookup"><span data-stu-id="50dea-108">Delete a DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="50dea-109">示例</span><span class="sxs-lookup"><span data-stu-id="50dea-109">EXAMPLES</span></span>

### <span data-ttu-id="50dea-110">範例1：依點終結點刪除 azDigitalTwinsEndPoint</span><span class="sxs-lookup"><span data-stu-id="50dea-110">Example 1: Delete the azDigitalTwinsEndPoint by EndPointName</span></span>
```powershell
PS C:\> Remove-AzDigitalTwinsEndpoint -ResourceGroupName youritemp -EndpointName youriEHEndpoint -ResourceName youriDigitalTwinsTest

```

<span data-ttu-id="50dea-111">依點 azDigitalTwinsEndPoint ResourceGroupName 和 CoNtext.resourcename 刪除</span><span class="sxs-lookup"><span data-stu-id="50dea-111">Delete the azDigitalTwinsEndPoint by EndPointName ResourceGroupName and ResourceName</span></span>

### <span data-ttu-id="50dea-112">範例2：刪除 azDigitalTwinsEndPoint 依據物件</span><span class="sxs-lookup"><span data-stu-id="50dea-112">Example 2: Delete the azDigitalTwinsEndPoint by Object</span></span>
```powershell
PS C:\> $GetAzdigitalTwinsEndpoint = Get-AzDigitalTwinsEndpoint -EndpointName youriEHEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Remove-AzDigitalTwinsEndpoint -InputObject $GetAzdigitalTwinsEndpoint

```

<span data-ttu-id="50dea-113">刪除 azDigitalTwinsEndPoint 依據物件</span><span class="sxs-lookup"><span data-stu-id="50dea-113">Delete the azDigitalTwinsEndPoint by Object</span></span>

## <span data-ttu-id="50dea-114">參數</span><span class="sxs-lookup"><span data-stu-id="50dea-114">PARAMETERS</span></span>

### <span data-ttu-id="50dea-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50dea-115">-AsJob</span></span>
<span data-ttu-id="50dea-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="50dea-116">Run the command as a job</span></span>

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

### <span data-ttu-id="50dea-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50dea-117">-DefaultProfile</span></span>
<span data-ttu-id="50dea-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="50dea-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50dea-119">-終結點</span><span class="sxs-lookup"><span data-stu-id="50dea-119">-EndpointName</span></span>
<span data-ttu-id="50dea-120">端點資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="50dea-120">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="50dea-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50dea-121">-InputObject</span></span>
<span data-ttu-id="50dea-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="50dea-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="50dea-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="50dea-123">-NoWait</span></span>
<span data-ttu-id="50dea-124">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="50dea-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="50dea-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="50dea-125">-PassThru</span></span>
<span data-ttu-id="50dea-126">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="50dea-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="50dea-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50dea-127">-ResourceGroupName</span></span>
<span data-ttu-id="50dea-128">包含 DigitalTwinsInstance 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="50dea-128">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="50dea-129">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="50dea-129">-ResourceName</span></span>
<span data-ttu-id="50dea-130">DigitalTwinsInstance 的名稱。</span><span class="sxs-lookup"><span data-stu-id="50dea-130">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="50dea-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="50dea-131">-SubscriptionId</span></span>
<span data-ttu-id="50dea-132">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="50dea-132">The subscription identifier.</span></span>

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

### <span data-ttu-id="50dea-133">-確認</span><span class="sxs-lookup"><span data-stu-id="50dea-133">-Confirm</span></span>
<span data-ttu-id="50dea-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="50dea-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50dea-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50dea-135">-WhatIf</span></span>
<span data-ttu-id="50dea-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="50dea-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50dea-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="50dea-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50dea-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50dea-138">CommonParameters</span></span>
<span data-ttu-id="50dea-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="50dea-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50dea-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="50dea-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50dea-141">輸入</span><span class="sxs-lookup"><span data-stu-id="50dea-141">INPUTS</span></span>

### <span data-ttu-id="50dea-142">IDigitalTwinsIdentity （DigitalTwins）的</span><span class="sxs-lookup"><span data-stu-id="50dea-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="50dea-143">輸出</span><span class="sxs-lookup"><span data-stu-id="50dea-143">OUTPUTS</span></span>

### <span data-ttu-id="50dea-144">IDigitalTwinsEndpointResource （DigitalTwins）。 Api20201031。</span><span class="sxs-lookup"><span data-stu-id="50dea-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="50dea-145">筆記</span><span class="sxs-lookup"><span data-stu-id="50dea-145">NOTES</span></span>

<span data-ttu-id="50dea-146">別名</span><span class="sxs-lookup"><span data-stu-id="50dea-146">ALIASES</span></span>

<span data-ttu-id="50dea-147">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="50dea-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="50dea-148">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="50dea-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="50dea-149">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="50dea-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="50dea-150">INPUTOBJECT <IDigitalTwinsIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="50dea-150">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="50dea-151">`[EndpointName <String>]`：端點資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="50dea-151">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="50dea-152">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="50dea-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="50dea-153">`[Location <String>]`： DigitalTwinsInstance 的位置。</span><span class="sxs-lookup"><span data-stu-id="50dea-153">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="50dea-154">`[ResourceGroupName <String>]`：包含 DigitalTwinsInstance 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="50dea-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="50dea-155">`[ResourceName <String>]`： DigitalTwinsInstance 的名稱。</span><span class="sxs-lookup"><span data-stu-id="50dea-155">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="50dea-156">`[SubscriptionId <String>]`：訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="50dea-156">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="50dea-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="50dea-157">RELATED LINKS</span></span>

