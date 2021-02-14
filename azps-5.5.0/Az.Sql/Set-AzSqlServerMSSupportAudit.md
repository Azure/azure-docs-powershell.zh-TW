---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Set-AzSqlServerMSSupportAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerMSSupportAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerMSSupportAudit.md
ms.openlocfilehash: 623f52f1de9370c679f6df09b6cf05c50f38ca6b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142954"
---
# <span data-ttu-id="33acb-101">Set-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="33acb-101">Set-AzSqlServerMSSupportAudit</span></span>

## <span data-ttu-id="33acb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="33acb-102">SYNOPSIS</span></span>
<span data-ttu-id="33acb-103">變更 Azure SQL server 的 Microsoft 支援作業審核設定。</span><span class="sxs-lookup"><span data-stu-id="33acb-103">Changes the Microsoft support operations auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="33acb-104">句法</span><span class="sxs-lookup"><span data-stu-id="33acb-104">SYNTAX</span></span>

### <span data-ttu-id="33acb-105">ServerParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="33acb-105">ServerParameterSet (Default)</span></span>
```
Set-AzSqlServerMSSupportAudit
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-EventHubTargetState <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>]
 [-LogAnalyticsTargetState <String>] [-WorkspaceResourceId <String>]
 [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33acb-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="33acb-106">ServerObjectParameterSet</span></span>
```
Set-AzSqlServerMSSupportAudit [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33acb-107">說明</span><span class="sxs-lookup"><span data-stu-id="33acb-107">DESCRIPTION</span></span>
<span data-ttu-id="33acb-108">**AzSqlServerMSSupportAudit** Cmdlet 會變更 Azure SQL Server 的 Microsoft 支援作業審核設定。</span><span class="sxs-lookup"><span data-stu-id="33acb-108">The **Set-AzSqlServerMSSupportAudit** cmdlet changes the  Microsoft support operations auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="33acb-109">若要使用 Cmdlet，請使用 *ResourceGroupName* 和 *ServerName* 參數來識別伺服器。</span><span class="sxs-lookup"><span data-stu-id="33acb-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="33acb-110">當 blob 儲存為審核記錄的目的地時，請指定 *StorageAccountResourceId* 參數來判斷審核記錄的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="33acb-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs.</span></span>

## <span data-ttu-id="33acb-111">示例</span><span class="sxs-lookup"><span data-stu-id="33acb-111">EXAMPLES</span></span>

### <span data-ttu-id="33acb-112">範例1：啟用 Azure SQL server 的 blob 儲存 Microsoft 支援作業審核原則</span><span class="sxs-lookup"><span data-stu-id="33acb-112">Example 1: Enable the blob storage Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="33acb-113">範例2：停用 Azure SQL server 的 blob 儲存 Microsoft 支援作業審核原則</span><span class="sxs-lookup"><span data-stu-id="33acb-113">Example 2: Disable the blob storage Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="33acb-114">範例3：啟用 Azure SQL server 的事件中心 Microsoft 支援作業審核原則</span><span class="sxs-lookup"><span data-stu-id="33acb-114">Example 3: Enable the event hub Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="33acb-115">範例4：停用 Azure SQL server 的事件中心 Microsoft 支援作業審核原則</span><span class="sxs-lookup"><span data-stu-id="33acb-115">Example 4: Disable the event hub Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Disabled
```

### <span data-ttu-id="33acb-116">範例5：啟用 Azure SQL server 的 log analytics Microsoft 支援作業審核原則</span><span class="sxs-lookup"><span data-stu-id="33acb-116">Example 5: Enable the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="33acb-117">範例6：停用 Azure SQL server 的 log analytics Microsoft 支援作業審核原則</span><span class="sxs-lookup"><span data-stu-id="33acb-117">Example 6: Disable the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="33acb-118">範例7：透過流水線來停用 Azure SQL server 的 log analytics Microsoft 支援作業審核原則</span><span class="sxs-lookup"><span data-stu-id="33acb-118">Example 7: Disable, through pipeline, the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerMSSupportAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="33acb-119">範例8：停用將 Azure SQL server 的 [Microsoft 支援作業] 審核記錄傳送到 [blob 儲存空間]，並啟用將其傳送至記錄分析的功能。</span><span class="sxs-lookup"><span data-stu-id="33acb-119">Example 8: Disable sending Microsoft support operations audit records of an Azure SQL server to blob storage, and enable sending them to log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="33acb-120">範例9：啟用將 Azure SQL server 的 [傳送 Microsoft 支援作業] 審核記錄傳送到 blob 儲存體、事件中樞和記錄分析。</span><span class="sxs-lookup"><span data-stu-id="33acb-120">Example 9: Enable sending Microsoft support operations audit records of an Azure SQL server to blob storage, event hub and log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="33acb-121">參數</span><span class="sxs-lookup"><span data-stu-id="33acb-121">PARAMETERS</span></span>

### <span data-ttu-id="33acb-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33acb-122">-AsJob</span></span>
<span data-ttu-id="33acb-123">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="33acb-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="33acb-124">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="33acb-124">-BlobStorageTargetState</span></span>
<span data-ttu-id="33acb-125">指出 [blob 儲存空間] 是否為 Microsoft 支援作業審計記錄的目的地。</span><span class="sxs-lookup"><span data-stu-id="33acb-125">Indicates whether blob storage is a destination for Microsoft support operations audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33acb-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33acb-126">-DefaultProfile</span></span>
<span data-ttu-id="33acb-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="33acb-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33acb-128">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="33acb-128">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="33acb-129">事件中心授權規則的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="33acb-129">The resource Id for the event hub authorization rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33acb-130">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="33acb-130">-EventHubName</span></span>
<span data-ttu-id="33acb-131">事件中心的名稱。</span><span class="sxs-lookup"><span data-stu-id="33acb-131">The name of the event hub.</span></span> <span data-ttu-id="33acb-132">如果在提供 EventHubAuthorizationRuleResourceId 時沒有指定，則會選取預設事件中樞。</span><span class="sxs-lookup"><span data-stu-id="33acb-132">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33acb-133">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="33acb-133">-EventHubTargetState</span></span>
<span data-ttu-id="33acb-134">指出事件中樞是否為 Microsoft 支援作業審計記錄的目的地。</span><span class="sxs-lookup"><span data-stu-id="33acb-134">Indicates whether event hub is a destination for Microsoft support operations audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33acb-135">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="33acb-135">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="33acb-136">指出 log analytics 是否為 Microsoft 支援作業審計記錄的目的地。</span><span class="sxs-lookup"><span data-stu-id="33acb-136">Indicates whether log analytics is a destination for Microsoft support operations audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33acb-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33acb-137">-PassThru</span></span>
<span data-ttu-id="33acb-138">指定是否要在 Cmdlet 執行結束時輸出 Microsoft 支援作業審核原則</span><span class="sxs-lookup"><span data-stu-id="33acb-138">Specifies whether to output the Microsoft support operations auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="33acb-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33acb-139">-ResourceGroupName</span></span>
<span data-ttu-id="33acb-140">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="33acb-140">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33acb-141">-ServerName</span><span class="sxs-lookup"><span data-stu-id="33acb-141">-ServerName</span></span>
<span data-ttu-id="33acb-142">SQL server 名稱。</span><span class="sxs-lookup"><span data-stu-id="33acb-142">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33acb-143">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="33acb-143">-ServerObject</span></span>
<span data-ttu-id="33acb-144">伺服器物件來管理其 Microsoft 支援作業的審核原則。</span><span class="sxs-lookup"><span data-stu-id="33acb-144">The server object to manage its Microsoft support operations audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ServerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33acb-145">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="33acb-145">-StorageAccountResourceId</span></span>
<span data-ttu-id="33acb-146">儲存空間帳戶資源識別碼</span><span class="sxs-lookup"><span data-stu-id="33acb-146">The storage account resource id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33acb-147">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="33acb-147">-WorkspaceResourceId</span></span>
<span data-ttu-id="33acb-148">您想要傳送 Microsoft 支援作業審核記錄的 Log analytics 工作區) 的 [工作區識別碼] (資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="33acb-148">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Microsoft support operations Audit Logs.</span></span> <span data-ttu-id="33acb-149">範例：/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="33acb-149">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33acb-150">-確認</span><span class="sxs-lookup"><span data-stu-id="33acb-150">-Confirm</span></span>
<span data-ttu-id="33acb-151">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="33acb-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33acb-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33acb-152">-WhatIf</span></span>
<span data-ttu-id="33acb-153">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="33acb-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="33acb-154">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="33acb-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33acb-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33acb-155">CommonParameters</span></span>
<span data-ttu-id="33acb-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="33acb-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33acb-157">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="33acb-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33acb-158">輸入</span><span class="sxs-lookup"><span data-stu-id="33acb-158">INPUTS</span></span>

### <span data-ttu-id="33acb-159">System.object</span><span class="sxs-lookup"><span data-stu-id="33acb-159">System.String</span></span>

### <span data-ttu-id="33acb-160">AzureSqlServerModel 的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="33acb-160">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="33acb-161">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="33acb-161">System.Guid</span></span>

### <span data-ttu-id="33acb-162">系統. Nullable "1 [[System. UInt32，System.object CoreLib，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="33acb-162">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="33acb-163">ServerDevOpsAuditModel （.Sql） .Sql。</span><span class="sxs-lookup"><span data-stu-id="33acb-163">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerDevOpsAuditModel</span></span>

## <span data-ttu-id="33acb-164">輸出</span><span class="sxs-lookup"><span data-stu-id="33acb-164">OUTPUTS</span></span>

### <span data-ttu-id="33acb-165">System.object</span><span class="sxs-lookup"><span data-stu-id="33acb-165">System.Boolean</span></span>

## <span data-ttu-id="33acb-166">筆記</span><span class="sxs-lookup"><span data-stu-id="33acb-166">NOTES</span></span>

## <span data-ttu-id="33acb-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="33acb-167">RELATED LINKS</span></span>
