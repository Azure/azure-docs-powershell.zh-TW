---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/remove-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Remove-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Remove-AzCommunicationService.md
ms.openlocfilehash: c165f9d69b18631f53bdc9444a623f43599532fa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449904"
---
# <span data-ttu-id="eb0fc-101">Remove-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="eb0fc-101">Remove-AzCommunicationService</span></span>

## <span data-ttu-id="eb0fc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eb0fc-102">SYNOPSIS</span></span>
<span data-ttu-id="eb0fc-103">刪除 CommunicationService 的操作。</span><span class="sxs-lookup"><span data-stu-id="eb0fc-103">Operation to delete a CommunicationService.</span></span>

## <span data-ttu-id="eb0fc-104">句法</span><span class="sxs-lookup"><span data-stu-id="eb0fc-104">SYNTAX</span></span>

### <span data-ttu-id="eb0fc-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="eb0fc-105">Delete (Default)</span></span>
```
Remove-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="eb0fc-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="eb0fc-106">DeleteViaIdentity</span></span>
```
Remove-AzCommunicationService -InputObject <ICommunicationIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="eb0fc-107">說明</span><span class="sxs-lookup"><span data-stu-id="eb0fc-107">DESCRIPTION</span></span>
<span data-ttu-id="eb0fc-108">刪除 CommunicationService 的操作。</span><span class="sxs-lookup"><span data-stu-id="eb0fc-108">Operation to delete a CommunicationService.</span></span>

## <span data-ttu-id="eb0fc-109">示例</span><span class="sxs-lookup"><span data-stu-id="eb0fc-109">EXAMPLES</span></span>

### <span data-ttu-id="eb0fc-110">範例1：移除指定的 Azure 通訊資源</span><span class="sxs-lookup"><span data-stu-id="eb0fc-110">Example 1: Remove the specified Azure Communication resource</span></span>
```powershell
PS C:\> Remove-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1
```

<span data-ttu-id="eb0fc-111">移除/刪除 Azure 通訊資源。</span><span class="sxs-lookup"><span data-stu-id="eb0fc-111">Remove / Delete the Azure Communication resource.</span></span>

## <span data-ttu-id="eb0fc-112">參數</span><span class="sxs-lookup"><span data-stu-id="eb0fc-112">PARAMETERS</span></span>

### <span data-ttu-id="eb0fc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb0fc-113">-AsJob</span></span>
<span data-ttu-id="eb0fc-114">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="eb0fc-114">Run the command as a job</span></span>

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

### <span data-ttu-id="eb0fc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb0fc-115">-DefaultProfile</span></span>
<span data-ttu-id="eb0fc-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eb0fc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb0fc-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb0fc-117">-InputObject</span></span>
<span data-ttu-id="eb0fc-118">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="eb0fc-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="eb0fc-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="eb0fc-119">-Name</span></span>
<span data-ttu-id="eb0fc-120">CommunicationService 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="eb0fc-120">The name of the CommunicationService resource.</span></span>

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

### <span data-ttu-id="eb0fc-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="eb0fc-121">-NoWait</span></span>
<span data-ttu-id="eb0fc-122">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="eb0fc-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="eb0fc-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb0fc-123">-PassThru</span></span>
<span data-ttu-id="eb0fc-124">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="eb0fc-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="eb0fc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb0fc-125">-ResourceGroupName</span></span>
<span data-ttu-id="eb0fc-126">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="eb0fc-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="eb0fc-127">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="eb0fc-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="eb0fc-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eb0fc-128">-SubscriptionId</span></span>
<span data-ttu-id="eb0fc-129">取得唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="eb0fc-129">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="eb0fc-130">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="eb0fc-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="eb0fc-131">-確認</span><span class="sxs-lookup"><span data-stu-id="eb0fc-131">-Confirm</span></span>
<span data-ttu-id="eb0fc-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="eb0fc-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb0fc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb0fc-133">-WhatIf</span></span>
<span data-ttu-id="eb0fc-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eb0fc-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb0fc-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eb0fc-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb0fc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb0fc-136">CommonParameters</span></span>
<span data-ttu-id="eb0fc-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eb0fc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb0fc-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="eb0fc-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb0fc-139">輸入</span><span class="sxs-lookup"><span data-stu-id="eb0fc-139">INPUTS</span></span>

### <span data-ttu-id="eb0fc-140">ICommunicationIdentity 中的 [Azure. Cmdlet]</span><span class="sxs-lookup"><span data-stu-id="eb0fc-140">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="eb0fc-141">輸出</span><span class="sxs-lookup"><span data-stu-id="eb0fc-141">OUTPUTS</span></span>

### <span data-ttu-id="eb0fc-142">System.object</span><span class="sxs-lookup"><span data-stu-id="eb0fc-142">System.Boolean</span></span>

## <span data-ttu-id="eb0fc-143">筆記</span><span class="sxs-lookup"><span data-stu-id="eb0fc-143">NOTES</span></span>

<span data-ttu-id="eb0fc-144">別名</span><span class="sxs-lookup"><span data-stu-id="eb0fc-144">ALIASES</span></span>

<span data-ttu-id="eb0fc-145">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="eb0fc-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="eb0fc-146">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="eb0fc-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="eb0fc-147">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="eb0fc-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="eb0fc-148">INPUTOBJECT <ICommunicationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="eb0fc-148">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="eb0fc-149">`[CommunicationServiceName <String>]`： CommunicationService 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="eb0fc-149">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="eb0fc-150">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="eb0fc-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="eb0fc-151">`[Location <String>]`： Azure 區域</span><span class="sxs-lookup"><span data-stu-id="eb0fc-151">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="eb0fc-152">`[OperationId <String>]`：正在進行中的非同步作業識別碼</span><span class="sxs-lookup"><span data-stu-id="eb0fc-152">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="eb0fc-153">`[ResourceGroupName <String>]`：包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="eb0fc-153">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="eb0fc-154">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="eb0fc-154">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="eb0fc-155">`[SubscriptionId <String>]`：取得唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="eb0fc-155">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="eb0fc-156">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="eb0fc-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="eb0fc-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="eb0fc-157">RELATED LINKS</span></span>

