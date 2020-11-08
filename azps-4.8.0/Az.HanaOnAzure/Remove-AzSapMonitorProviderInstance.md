---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/remove-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitorProviderInstance.md
ms.openlocfilehash: 53f251b001b4e2f6319840079e9db3111c00b006
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127698"
---
# <span data-ttu-id="f0597-101">Remove-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="f0597-101">Remove-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="f0597-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f0597-102">SYNOPSIS</span></span>
<span data-ttu-id="f0597-103">刪除指定訂閱、資源群組、SapMonitor 名稱和資源名稱的提供者實例。</span><span class="sxs-lookup"><span data-stu-id="f0597-103">Deletes a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="f0597-104">句法</span><span class="sxs-lookup"><span data-stu-id="f0597-104">SYNTAX</span></span>

### <span data-ttu-id="f0597-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="f0597-105">Delete (Default)</span></span>
```
Remove-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="f0597-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f0597-106">DeleteViaIdentity</span></span>
```
Remove-AzSapMonitorProviderInstance -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f0597-107">說明</span><span class="sxs-lookup"><span data-stu-id="f0597-107">DESCRIPTION</span></span>
<span data-ttu-id="f0597-108">刪除指定訂閱、資源群組、SapMonitor 名稱和資源名稱的提供者實例。</span><span class="sxs-lookup"><span data-stu-id="f0597-108">Deletes a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="f0597-109">示例</span><span class="sxs-lookup"><span data-stu-id="f0597-109">EXAMPLES</span></span>

### <span data-ttu-id="f0597-110">範例1：依名稱移除 SAP 監視器的實例</span><span class="sxs-lookup"><span data-stu-id="f0597-110">Example 1: Remove instance of SAP monitor by name</span></span>
```powershell
PS C:\> Remove-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02

```

<span data-ttu-id="f0597-111">這個命令會依名稱移除 SAP 監視器的實例。</span><span class="sxs-lookup"><span data-stu-id="f0597-111">This command removes instance of SAP monitor by name.</span></span>

### <span data-ttu-id="f0597-112">範例2：依物件移除 SAP monitor 的實例</span><span class="sxs-lookup"><span data-stu-id="f0597-112">Example 2: Remove instance of SAP monitor by object</span></span>
```powershell
PS C:\> $sapIns = Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t01
PS C:\> Remove-AzSapMonitorProviderInstance -InputObject $sapIns

```

<span data-ttu-id="f0597-113">這個命令會移除 SAP monitor by 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="f0597-113">This command removes instance of SAP monitor by object.</span></span>

## <span data-ttu-id="f0597-114">參數</span><span class="sxs-lookup"><span data-stu-id="f0597-114">PARAMETERS</span></span>

### <span data-ttu-id="f0597-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0597-115">-AsJob</span></span>
<span data-ttu-id="f0597-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="f0597-116">Run the command as a job</span></span>

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

### <span data-ttu-id="f0597-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0597-117">-DefaultProfile</span></span>
<span data-ttu-id="f0597-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f0597-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0597-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0597-119">-InputObject</span></span>
<span data-ttu-id="f0597-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f0597-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f0597-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="f0597-121">-Name</span></span>
<span data-ttu-id="f0597-122">提供者實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="f0597-122">Name of the provider instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ProviderInstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0597-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f0597-123">-NoWait</span></span>
<span data-ttu-id="f0597-124">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="f0597-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f0597-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0597-125">-PassThru</span></span>
<span data-ttu-id="f0597-126">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="f0597-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f0597-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0597-127">-ResourceGroupName</span></span>
<span data-ttu-id="f0597-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f0597-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="f0597-129">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="f0597-129">-SapMonitorName</span></span>
<span data-ttu-id="f0597-130">SAP 監視資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="f0597-130">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="f0597-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f0597-131">-SubscriptionId</span></span>
<span data-ttu-id="f0597-132">訂閱識別碼，可唯一識別 Microsoft Azure 訂閱。</span><span class="sxs-lookup"><span data-stu-id="f0597-132">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f0597-133">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="f0597-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f0597-134">-確認</span><span class="sxs-lookup"><span data-stu-id="f0597-134">-Confirm</span></span>
<span data-ttu-id="f0597-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f0597-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0597-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0597-136">-WhatIf</span></span>
<span data-ttu-id="f0597-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f0597-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0597-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f0597-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0597-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0597-139">CommonParameters</span></span>
<span data-ttu-id="f0597-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f0597-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0597-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f0597-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0597-142">輸入</span><span class="sxs-lookup"><span data-stu-id="f0597-142">INPUTS</span></span>

### <span data-ttu-id="f0597-143">IHanaOnAzureIdentity （HanaOnAzure）的</span><span class="sxs-lookup"><span data-stu-id="f0597-143">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="f0597-144">輸出</span><span class="sxs-lookup"><span data-stu-id="f0597-144">OUTPUTS</span></span>

### <span data-ttu-id="f0597-145">System.object</span><span class="sxs-lookup"><span data-stu-id="f0597-145">System.Boolean</span></span>

## <span data-ttu-id="f0597-146">筆記</span><span class="sxs-lookup"><span data-stu-id="f0597-146">NOTES</span></span>

<span data-ttu-id="f0597-147">別名</span><span class="sxs-lookup"><span data-stu-id="f0597-147">ALIASES</span></span>

<span data-ttu-id="f0597-148">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="f0597-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f0597-149">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="f0597-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f0597-150">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="f0597-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f0597-151">INPUTOBJECT <IHanaOnAzureIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="f0597-151">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f0597-152">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="f0597-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f0597-153">`[Location <String>]`：已刪除的保存庫的位置。</span><span class="sxs-lookup"><span data-stu-id="f0597-153">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="f0597-154">`[OperationKind <AccessPolicyUpdateKind?>]`：操作的名稱</span><span class="sxs-lookup"><span data-stu-id="f0597-154">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="f0597-155">`[ProviderInstanceName <String>]`：提供者實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="f0597-155">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="f0597-156">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f0597-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="f0597-157">`[ResourceName <String>]`：身分識別資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="f0597-157">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="f0597-158">`[SapMonitorName <String>]`： SAP 監視器資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="f0597-158">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="f0597-159">`[Scope <String>]`：資源的資源提供者範圍。</span><span class="sxs-lookup"><span data-stu-id="f0597-159">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="f0597-160">受管理的身分識別的父資源。</span><span class="sxs-lookup"><span data-stu-id="f0597-160">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="f0597-161">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="f0597-161">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f0597-162">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="f0597-162">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="f0597-163">`[VaultName <String>]`：保存庫的名稱</span><span class="sxs-lookup"><span data-stu-id="f0597-163">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="f0597-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="f0597-164">RELATED LINKS</span></span>
