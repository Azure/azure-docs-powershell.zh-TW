---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 87c3f0e2e86f2867d659b26b5acc9df5a6dfe8c7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142371"
---
# <span data-ttu-id="259c0-101">Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="259c0-101">Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="259c0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="259c0-102">SYNOPSIS</span></span>
<span data-ttu-id="259c0-103">在 SQL 池中設定高級威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="259c0-103">Sets a advanced threat protection settings on a SQL pool.</span></span>

## <span data-ttu-id="259c0-104">句法</span><span class="sxs-lookup"><span data-stu-id="259c0-104">SYNTAX</span></span>

### <span data-ttu-id="259c0-105">UpdateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="259c0-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>]
 [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="259c0-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="259c0-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="259c0-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="259c0-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="259c0-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="259c0-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="259c0-109">說明</span><span class="sxs-lookup"><span data-stu-id="259c0-109">DESCRIPTION</span></span>
<span data-ttu-id="259c0-110">**AzSynapseSqlPoolAdvancedThreatProtectionSetting** Cmdlet 會在 Azure SYNAPSE Analytics SQL pool 上設定高級威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="259c0-110">The **Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure Synapse Analytics SQL pool.</span></span>
<span data-ttu-id="259c0-111">為了在 SQL 池中啟用高級威脅防護，必須在該 SQL 池中啟用 [審核] 設定。</span><span class="sxs-lookup"><span data-stu-id="259c0-111">In order to enable advanced threat protection on a SQL pool an auditing settings must be enabled on that SQL pool.</span></span>

## <span data-ttu-id="259c0-112">示例</span><span class="sxs-lookup"><span data-stu-id="259c0-112">EXAMPLES</span></span>

### <span data-ttu-id="259c0-113">範例1</span><span class="sxs-lookup"><span data-stu-id="259c0-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="259c0-114">這個命令會在名為 [ContosoWorkspace] 的工作區下，為名為「ContosoSqlPool」的 SQL pool 設定高級威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="259c0-114">This command sets the advanced threat protection settings for a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="259c0-115">參數</span><span class="sxs-lookup"><span data-stu-id="259c0-115">PARAMETERS</span></span>

### <span data-ttu-id="259c0-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="259c0-116">-AsJob</span></span>
<span data-ttu-id="259c0-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="259c0-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="259c0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="259c0-118">-DefaultProfile</span></span>
<span data-ttu-id="259c0-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="259c0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="259c0-120">-EmailAdmin</span><span class="sxs-lookup"><span data-stu-id="259c0-120">-EmailAdmin</span></span>
<span data-ttu-id="259c0-121">定義是否要傳送電子郵件給系統管理員。</span><span class="sxs-lookup"><span data-stu-id="259c0-121">Defines whether to email administrators.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: EmailAdmins

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="259c0-122">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="259c0-122">-ExcludedDetectionType</span></span>
<span data-ttu-id="259c0-123">要排除的偵測類型。</span><span class="sxs-lookup"><span data-stu-id="259c0-123">Detection types to exclude.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="259c0-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="259c0-124">-InputObject</span></span>
<span data-ttu-id="259c0-125">SQL pool 輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="259c0-125">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="259c0-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="259c0-126">-Name</span></span>
<span data-ttu-id="259c0-127">Synapse SQL pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="259c0-127">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="259c0-128">-NotificationRecipientsEmail</span><span class="sxs-lookup"><span data-stu-id="259c0-128">-NotificationRecipientsEmail</span></span>
<span data-ttu-id="259c0-129">要傳送提醒的電子郵件地址清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="259c0-129">A semicolon separated list of email addresses to send the alerts to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NotificationRecipientsEmails

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="259c0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="259c0-130">-ResourceGroupName</span></span>
<span data-ttu-id="259c0-131">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="259c0-131">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="259c0-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="259c0-132">-ResourceId</span></span>
<span data-ttu-id="259c0-133">Synapse SQL Pool 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="259c0-133">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="259c0-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="259c0-134">-RetentionInDays</span></span>
<span data-ttu-id="259c0-135">審計記錄的保留天數。</span><span class="sxs-lookup"><span data-stu-id="259c0-135">The number of retention days for the audit logs.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="259c0-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="259c0-136">-StorageAccountName</span></span>
<span data-ttu-id="259c0-137">儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="259c0-137">The name of the storage account.</span></span>

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

### <span data-ttu-id="259c0-138">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="259c0-138">-WorkspaceName</span></span>
<span data-ttu-id="259c0-139">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="259c0-139">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="259c0-140">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="259c0-140">-WorkspaceObject</span></span>
<span data-ttu-id="259c0-141">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="259c0-141">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="259c0-142">-確認</span><span class="sxs-lookup"><span data-stu-id="259c0-142">-Confirm</span></span>
<span data-ttu-id="259c0-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="259c0-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="259c0-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="259c0-144">-WhatIf</span></span>
<span data-ttu-id="259c0-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="259c0-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="259c0-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="259c0-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="259c0-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="259c0-147">CommonParameters</span></span>
<span data-ttu-id="259c0-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="259c0-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="259c0-149">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="259c0-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="259c0-150">輸入</span><span class="sxs-lookup"><span data-stu-id="259c0-150">INPUTS</span></span>

### <span data-ttu-id="259c0-151">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="259c0-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="259c0-152">PSSynapseSqlPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="259c0-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="259c0-153">輸出</span><span class="sxs-lookup"><span data-stu-id="259c0-153">OUTPUTS</span></span>

### <span data-ttu-id="259c0-154">PSSqlPoolSecurityAlertPolicy 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="259c0-154">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span></span>

## <span data-ttu-id="259c0-155">筆記</span><span class="sxs-lookup"><span data-stu-id="259c0-155">NOTES</span></span>

## <span data-ttu-id="259c0-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="259c0-156">RELATED LINKS</span></span>
