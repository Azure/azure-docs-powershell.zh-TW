---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/powershell/module/az.communication/remove-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Remove-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Remove-AzCommunicationService.md
ms.openlocfilehash: 3feb6e2246e2265c36e67d64621a5726eaabb6a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912081"
---
# <span data-ttu-id="37b65-101">Remove-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="37b65-101">Remove-AzCommunicationService</span></span>

## <span data-ttu-id="37b65-102">簡介</span><span class="sxs-lookup"><span data-stu-id="37b65-102">SYNOPSIS</span></span>
<span data-ttu-id="37b65-103">刪除 CommunicationService 的作業。</span><span class="sxs-lookup"><span data-stu-id="37b65-103">Operation to delete a CommunicationService.</span></span>

## <span data-ttu-id="37b65-104">語法</span><span class="sxs-lookup"><span data-stu-id="37b65-104">SYNTAX</span></span>

### <span data-ttu-id="37b65-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="37b65-105">Delete (Default)</span></span>
```
Remove-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="37b65-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="37b65-106">DeleteViaIdentity</span></span>
```
Remove-AzCommunicationService -InputObject <ICommunicationIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="37b65-107">描述</span><span class="sxs-lookup"><span data-stu-id="37b65-107">DESCRIPTION</span></span>
<span data-ttu-id="37b65-108">刪除 CommunicationService 的作業。</span><span class="sxs-lookup"><span data-stu-id="37b65-108">Operation to delete a CommunicationService.</span></span>

## <span data-ttu-id="37b65-109">例子</span><span class="sxs-lookup"><span data-stu-id="37b65-109">EXAMPLES</span></span>

### <span data-ttu-id="37b65-110">範例 1：移除指定的 Azure 通訊資源</span><span class="sxs-lookup"><span data-stu-id="37b65-110">Example 1: Remove the specified Azure Communication resource</span></span>
```powershell
PS C:\> Remove-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1
```

<span data-ttu-id="37b65-111">移除/刪除 Azure 通訊資源。</span><span class="sxs-lookup"><span data-stu-id="37b65-111">Remove / Delete the Azure Communication resource.</span></span>

## <span data-ttu-id="37b65-112">參數</span><span class="sxs-lookup"><span data-stu-id="37b65-112">PARAMETERS</span></span>

### <span data-ttu-id="37b65-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37b65-113">-AsJob</span></span>
<span data-ttu-id="37b65-114">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="37b65-114">Run the command as a job</span></span>

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

### <span data-ttu-id="37b65-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37b65-115">-DefaultProfile</span></span>
<span data-ttu-id="37b65-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="37b65-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37b65-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37b65-117">-InputObject</span></span>
<span data-ttu-id="37b65-118">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="37b65-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37b65-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="37b65-119">-Name</span></span>
<span data-ttu-id="37b65-120">CommunicationService 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="37b65-120">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37b65-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="37b65-121">-NoWait</span></span>
<span data-ttu-id="37b65-122">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="37b65-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="37b65-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37b65-123">-PassThru</span></span>
<span data-ttu-id="37b65-124">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="37b65-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="37b65-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37b65-125">-ResourceGroupName</span></span>
<span data-ttu-id="37b65-126">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="37b65-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="37b65-127">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="37b65-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="37b65-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="37b65-128">-SubscriptionId</span></span>
<span data-ttu-id="37b65-129">獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="37b65-129">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="37b65-130">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="37b65-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="37b65-131">-確認</span><span class="sxs-lookup"><span data-stu-id="37b65-131">-Confirm</span></span>
<span data-ttu-id="37b65-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="37b65-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37b65-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37b65-133">-WhatIf</span></span>
<span data-ttu-id="37b65-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="37b65-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37b65-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="37b65-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37b65-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37b65-136">CommonParameters</span></span>
<span data-ttu-id="37b65-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="37b65-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37b65-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37b65-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37b65-139">輸入</span><span class="sxs-lookup"><span data-stu-id="37b65-139">INPUTS</span></span>

### <span data-ttu-id="37b65-140">Microsoft.Azure.PowerShell.Cmdlets.Communication.models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="37b65-140">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="37b65-141">輸出</span><span class="sxs-lookup"><span data-stu-id="37b65-141">OUTPUTS</span></span>

### <span data-ttu-id="37b65-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="37b65-142">System.Boolean</span></span>

## <span data-ttu-id="37b65-143">筆記</span><span class="sxs-lookup"><span data-stu-id="37b65-143">NOTES</span></span>

<span data-ttu-id="37b65-144">別名</span><span class="sxs-lookup"><span data-stu-id="37b65-144">ALIASES</span></span>

<span data-ttu-id="37b65-145">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="37b65-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="37b65-146">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="37b65-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="37b65-147">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="37b65-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="37b65-148">INPUTOBJECT： <ICommunicationIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="37b65-148">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="37b65-149">`[CommunicationServiceName <String>]`：CommunicationService 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="37b65-149">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="37b65-150">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="37b65-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="37b65-151">`[Location <String>]`：Azure 區域</span><span class="sxs-lookup"><span data-stu-id="37b65-151">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="37b65-152">`[OperationId <String>]`：進行中的同步作業識別碼</span><span class="sxs-lookup"><span data-stu-id="37b65-152">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="37b65-153">`[ResourceGroupName <String>]`：包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="37b65-153">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="37b65-154">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="37b65-154">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="37b65-155">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="37b65-155">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="37b65-156">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="37b65-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="37b65-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="37b65-157">RELATED LINKS</span></span>

