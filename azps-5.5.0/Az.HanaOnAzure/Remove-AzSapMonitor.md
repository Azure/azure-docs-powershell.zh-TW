---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/remove-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitor.md
ms.openlocfilehash: bcba06d87bce2f9ccc8016afc9f08dff75e29b1c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131927"
---
# <span data-ttu-id="512ad-101">Remove-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="512ad-101">Remove-AzSapMonitor</span></span>

## <span data-ttu-id="512ad-102">摘要</span><span class="sxs-lookup"><span data-stu-id="512ad-102">SYNOPSIS</span></span>
<span data-ttu-id="512ad-103">刪除具有指定訂閱、資源群組和監視器名稱的 SAP 監視器。</span><span class="sxs-lookup"><span data-stu-id="512ad-103">Deletes a SAP monitor with the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="512ad-104">句法</span><span class="sxs-lookup"><span data-stu-id="512ad-104">SYNTAX</span></span>

### <span data-ttu-id="512ad-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="512ad-105">Delete (Default)</span></span>
```
Remove-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="512ad-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="512ad-106">DeleteViaIdentity</span></span>
```
Remove-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="512ad-107">說明</span><span class="sxs-lookup"><span data-stu-id="512ad-107">DESCRIPTION</span></span>
<span data-ttu-id="512ad-108">刪除具有指定訂閱、資源群組和監視器名稱的 SAP 監視器。</span><span class="sxs-lookup"><span data-stu-id="512ad-108">Deletes a SAP monitor with the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="512ad-109">示例</span><span class="sxs-lookup"><span data-stu-id="512ad-109">EXAMPLES</span></span>

### <span data-ttu-id="512ad-110">範例1：依名稱移除 SAP 監視器</span><span class="sxs-lookup"><span data-stu-id="512ad-110">Example 1: Remove a SAP monitor by name</span></span>
```powershell
PS C:\> Remove-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t02

```

<span data-ttu-id="512ad-111">這個命令會依名稱移除 SAP 監視器。</span><span class="sxs-lookup"><span data-stu-id="512ad-111">This command removes a SAP monitor by name.</span></span>

### <span data-ttu-id="512ad-112">範例2：依物件移除 SAP 監視器</span><span class="sxs-lookup"><span data-stu-id="512ad-112">Example 2: Remove a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t01
PS C:\> Remove-AzSapMonitor -InputObject $sap

```

<span data-ttu-id="512ad-113">這個命令會依物件移除 SAP 監視器。</span><span class="sxs-lookup"><span data-stu-id="512ad-113">This command removes a SAP monitor by object.</span></span>

## <span data-ttu-id="512ad-114">參數</span><span class="sxs-lookup"><span data-stu-id="512ad-114">PARAMETERS</span></span>

### <span data-ttu-id="512ad-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="512ad-115">-AsJob</span></span>
<span data-ttu-id="512ad-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="512ad-116">Run the command as a job</span></span>

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

### <span data-ttu-id="512ad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="512ad-117">-DefaultProfile</span></span>
<span data-ttu-id="512ad-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="512ad-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="512ad-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="512ad-119">-InputObject</span></span>
<span data-ttu-id="512ad-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="512ad-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="512ad-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="512ad-121">-Name</span></span>
<span data-ttu-id="512ad-122">SAP 監視資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="512ad-122">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="512ad-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="512ad-123">-NoWait</span></span>
<span data-ttu-id="512ad-124">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="512ad-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="512ad-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="512ad-125">-PassThru</span></span>
<span data-ttu-id="512ad-126">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="512ad-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="512ad-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="512ad-127">-ResourceGroupName</span></span>
<span data-ttu-id="512ad-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="512ad-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="512ad-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="512ad-129">-SubscriptionId</span></span>
<span data-ttu-id="512ad-130">訂閱識別碼，可唯一識別 Microsoft Azure 訂閱。</span><span class="sxs-lookup"><span data-stu-id="512ad-130">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="512ad-131">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="512ad-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="512ad-132">-確認</span><span class="sxs-lookup"><span data-stu-id="512ad-132">-Confirm</span></span>
<span data-ttu-id="512ad-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="512ad-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="512ad-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="512ad-134">-WhatIf</span></span>
<span data-ttu-id="512ad-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="512ad-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="512ad-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="512ad-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="512ad-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="512ad-137">CommonParameters</span></span>
<span data-ttu-id="512ad-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="512ad-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="512ad-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="512ad-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="512ad-140">輸入</span><span class="sxs-lookup"><span data-stu-id="512ad-140">INPUTS</span></span>

### <span data-ttu-id="512ad-141">IHanaOnAzureIdentity （HanaOnAzure）的</span><span class="sxs-lookup"><span data-stu-id="512ad-141">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="512ad-142">輸出</span><span class="sxs-lookup"><span data-stu-id="512ad-142">OUTPUTS</span></span>

### <span data-ttu-id="512ad-143">System.object</span><span class="sxs-lookup"><span data-stu-id="512ad-143">System.Boolean</span></span>

## <span data-ttu-id="512ad-144">筆記</span><span class="sxs-lookup"><span data-stu-id="512ad-144">NOTES</span></span>

<span data-ttu-id="512ad-145">別名</span><span class="sxs-lookup"><span data-stu-id="512ad-145">ALIASES</span></span>

<span data-ttu-id="512ad-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="512ad-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="512ad-147">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="512ad-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="512ad-148">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="512ad-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="512ad-149">INPUTOBJECT <IHanaOnAzureIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="512ad-149">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="512ad-150">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="512ad-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="512ad-151">`[Location <String>]`：已刪除的保存庫的位置。</span><span class="sxs-lookup"><span data-stu-id="512ad-151">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="512ad-152">`[OperationKind <AccessPolicyUpdateKind?>]`：操作的名稱</span><span class="sxs-lookup"><span data-stu-id="512ad-152">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="512ad-153">`[ProviderInstanceName <String>]`：提供者實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="512ad-153">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="512ad-154">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="512ad-154">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="512ad-155">`[ResourceName <String>]`：身分識別資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="512ad-155">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="512ad-156">`[SapMonitorName <String>]`： SAP 監視器資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="512ad-156">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="512ad-157">`[Scope <String>]`：資源的資源提供者範圍。</span><span class="sxs-lookup"><span data-stu-id="512ad-157">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="512ad-158">受管理的身分識別的父資源。</span><span class="sxs-lookup"><span data-stu-id="512ad-158">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="512ad-159">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="512ad-159">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="512ad-160">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="512ad-160">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="512ad-161">`[VaultName <String>]`：保存庫的名稱</span><span class="sxs-lookup"><span data-stu-id="512ad-161">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="512ad-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="512ad-162">RELATED LINKS</span></span>

