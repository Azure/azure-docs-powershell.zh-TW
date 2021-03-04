---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/Set-AzSqlServerMSSupportAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerMSSupportAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerMSSupportAudit.md
ms.openlocfilehash: 6e101beb73b68427f806fdae3fa2406082a9b47a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910358"
---
# <span data-ttu-id="119ea-101">Set-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="119ea-101">Set-AzSqlServerMSSupportAudit</span></span>

## <span data-ttu-id="119ea-102">簡介</span><span class="sxs-lookup"><span data-stu-id="119ea-102">SYNOPSIS</span></span>
<span data-ttu-id="119ea-103">變更 Azure SQL 伺服器的 Microsoft 支援作業稽核設定。</span><span class="sxs-lookup"><span data-stu-id="119ea-103">Changes the Microsoft support operations auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="119ea-104">語法</span><span class="sxs-lookup"><span data-stu-id="119ea-104">SYNTAX</span></span>

### <span data-ttu-id="119ea-105">ServerParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="119ea-105">ServerParameterSet (Default)</span></span>
```
Set-AzSqlServerMSSupportAudit
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-EventHubTargetState <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>]
 [-LogAnalyticsTargetState <String>] [-WorkspaceResourceId <String>]
 [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="119ea-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="119ea-106">ServerObjectParameterSet</span></span>
```
Set-AzSqlServerMSSupportAudit [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="119ea-107">描述</span><span class="sxs-lookup"><span data-stu-id="119ea-107">DESCRIPTION</span></span>
<span data-ttu-id="119ea-108">**Set-AzSqlServerMSSupportAudit** Cmdlet 會變更 Azure SQL 伺服器的 Microsoft 支援作業稽核設定。</span><span class="sxs-lookup"><span data-stu-id="119ea-108">The **Set-AzSqlServerMSSupportAudit** cmdlet changes the  Microsoft support operations auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="119ea-109">若要使用 Cmdlet，請使用 *ResourceGroupName* 和 *ServerName* 參數來識別伺服器。</span><span class="sxs-lookup"><span data-stu-id="119ea-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="119ea-110">當 Blob 儲存體是稽核記錄的目標時，請指定 *StorageAccountResourceId* 參數，以決定稽核記錄中的儲存帳戶。</span><span class="sxs-lookup"><span data-stu-id="119ea-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs.</span></span>

## <span data-ttu-id="119ea-111">例子</span><span class="sxs-lookup"><span data-stu-id="119ea-111">EXAMPLES</span></span>

### <span data-ttu-id="119ea-112">範例 1：啟用 Azure SQL Server 的 Blob 儲存空間 Microsoft 支援作業稽核策略</span><span class="sxs-lookup"><span data-stu-id="119ea-112">Example 1: Enable the blob storage Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="119ea-113">範例 2：停用 Azure SQL Server 的 Blob 儲存空間 Microsoft 支援作業稽核策略</span><span class="sxs-lookup"><span data-stu-id="119ea-113">Example 2: Disable the blob storage Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="119ea-114">範例 3：啟用 Azure SQL 伺服器的事件中樞 Microsoft 支援作業稽核策略</span><span class="sxs-lookup"><span data-stu-id="119ea-114">Example 3: Enable the event hub Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="119ea-115">範例 4：停用 Azure SQL 伺服器的事件中樞 Microsoft 支援作業稽核策略</span><span class="sxs-lookup"><span data-stu-id="119ea-115">Example 4: Disable the event hub Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Disabled
```

### <span data-ttu-id="119ea-116">範例 5：啟用 Azure SQL Server 的記錄分析 Microsoft 支援作業稽核策略</span><span class="sxs-lookup"><span data-stu-id="119ea-116">Example 5: Enable the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="119ea-117">範例 6：停用 Azure SQL Server 的記錄分析 Microsoft 支援作業稽核政策</span><span class="sxs-lookup"><span data-stu-id="119ea-117">Example 6: Disable the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="119ea-118">範例 7：透過管線停用記錄分析 Microsoft 支援 Azure SQL 伺服器的營運稽核政策</span><span class="sxs-lookup"><span data-stu-id="119ea-118">Example 7: Disable, through pipeline, the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerMSSupportAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="119ea-119">範例 8：停用將 Azure SQL Server 的 Microsoft 支援作業稽核記錄傳送至 Blob 儲存空間，並啟用傳送記錄分析。</span><span class="sxs-lookup"><span data-stu-id="119ea-119">Example 8: Disable sending Microsoft support operations audit records of an Azure SQL server to blob storage, and enable sending them to log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="119ea-120">範例 9：啟用將 Azure SQL Server 的 Microsoft 支援作業稽核記錄傳送至 Blob 儲存體、事件中樞和記錄分析。</span><span class="sxs-lookup"><span data-stu-id="119ea-120">Example 9: Enable sending Microsoft support operations audit records of an Azure SQL server to blob storage, event hub and log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="119ea-121">參數</span><span class="sxs-lookup"><span data-stu-id="119ea-121">PARAMETERS</span></span>

### <span data-ttu-id="119ea-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="119ea-122">-AsJob</span></span>
<span data-ttu-id="119ea-123">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="119ea-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="119ea-124">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="119ea-124">-BlobStorageTargetState</span></span>
<span data-ttu-id="119ea-125">指出 Blob 儲存空間是否是 Microsoft 支援作業稽核記錄的目的地。</span><span class="sxs-lookup"><span data-stu-id="119ea-125">Indicates whether blob storage is a destination for Microsoft support operations audit records.</span></span>

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

### <span data-ttu-id="119ea-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="119ea-126">-DefaultProfile</span></span>
<span data-ttu-id="119ea-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="119ea-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="119ea-128">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="119ea-128">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="119ea-129">事件中樞授權規則的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="119ea-129">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="119ea-130">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="119ea-130">-EventHubName</span></span>
<span data-ttu-id="119ea-131">事件中樞的名稱。</span><span class="sxs-lookup"><span data-stu-id="119ea-131">The name of the event hub.</span></span> <span data-ttu-id="119ea-132">如果在提供 EventHubAuthorizationRuleResourceId 時未指定任何專案，將會選取預設的事件中樞。</span><span class="sxs-lookup"><span data-stu-id="119ea-132">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="119ea-133">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="119ea-133">-EventHubTargetState</span></span>
<span data-ttu-id="119ea-134">指出事件中樞是否是 Microsoft 支援作業稽核記錄的目的地。</span><span class="sxs-lookup"><span data-stu-id="119ea-134">Indicates whether event hub is a destination for Microsoft support operations audit records.</span></span>

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

### <span data-ttu-id="119ea-135">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="119ea-135">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="119ea-136">指出記錄分析是否是 Microsoft 支援作業稽核記錄的目的地。</span><span class="sxs-lookup"><span data-stu-id="119ea-136">Indicates whether log analytics is a destination for Microsoft support operations audit records.</span></span>

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

### <span data-ttu-id="119ea-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="119ea-137">-PassThru</span></span>
<span data-ttu-id="119ea-138">指定是否要在 Cmdlet 執行結束時輸出 Microsoft 支援作業稽核政策</span><span class="sxs-lookup"><span data-stu-id="119ea-138">Specifies whether to output the Microsoft support operations auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="119ea-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="119ea-139">-ResourceGroupName</span></span>
<span data-ttu-id="119ea-140">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="119ea-140">The name of the resource group.</span></span>

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

### <span data-ttu-id="119ea-141">-ServerName</span><span class="sxs-lookup"><span data-stu-id="119ea-141">-ServerName</span></span>
<span data-ttu-id="119ea-142">SQL 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="119ea-142">SQL server name.</span></span>

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

### <span data-ttu-id="119ea-143">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="119ea-143">-ServerObject</span></span>
<span data-ttu-id="119ea-144">管理其 Microsoft 支援作業稽核策略的伺服器物件。</span><span class="sxs-lookup"><span data-stu-id="119ea-144">The server object to manage its Microsoft support operations audit policy.</span></span>

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

### <span data-ttu-id="119ea-145">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="119ea-145">-StorageAccountResourceId</span></span>
<span data-ttu-id="119ea-146">儲存帳戶資源識別碼</span><span class="sxs-lookup"><span data-stu-id="119ea-146">The storage account resource id</span></span>

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

### <span data-ttu-id="119ea-147">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="119ea-147">-WorkspaceResourceId</span></span>
<span data-ttu-id="119ea-148">針對要 (Microsoft 支援作業稽核記錄) 記錄分析工作區的工作區識別碼或資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="119ea-148">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Microsoft support operations Audit Logs.</span></span> <span data-ttu-id="119ea-149">範例：/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="119ea-149">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="119ea-150">-確認</span><span class="sxs-lookup"><span data-stu-id="119ea-150">-Confirm</span></span>
<span data-ttu-id="119ea-151">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="119ea-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="119ea-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="119ea-152">-WhatIf</span></span>
<span data-ttu-id="119ea-153">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="119ea-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="119ea-154">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="119ea-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="119ea-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="119ea-155">CommonParameters</span></span>
<span data-ttu-id="119ea-156">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="119ea-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="119ea-157">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="119ea-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="119ea-158">輸入</span><span class="sxs-lookup"><span data-stu-id="119ea-158">INPUTS</span></span>

### <span data-ttu-id="119ea-159">System.String</span><span class="sxs-lookup"><span data-stu-id="119ea-159">System.String</span></span>

### <span data-ttu-id="119ea-160">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="119ea-160">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="119ea-161">System.Guid</span><span class="sxs-lookup"><span data-stu-id="119ea-161">System.Guid</span></span>

### <span data-ttu-id="119ea-162">System.Nullable'1[[System.UInt32， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="119ea-162">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="119ea-163">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerDevOpsAuditModel</span><span class="sxs-lookup"><span data-stu-id="119ea-163">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerDevOpsAuditModel</span></span>

## <span data-ttu-id="119ea-164">輸出</span><span class="sxs-lookup"><span data-stu-id="119ea-164">OUTPUTS</span></span>

### <span data-ttu-id="119ea-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="119ea-165">System.Boolean</span></span>

## <span data-ttu-id="119ea-166">筆記</span><span class="sxs-lookup"><span data-stu-id="119ea-166">NOTES</span></span>

## <span data-ttu-id="119ea-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="119ea-167">RELATED LINKS</span></span>
