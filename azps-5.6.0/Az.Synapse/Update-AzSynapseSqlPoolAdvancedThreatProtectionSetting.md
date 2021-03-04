---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 2267f9420e545fd693b734aaf8f90e89cce000a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912974"
---
# <span data-ttu-id="31bbd-101">Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="31bbd-101">Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="31bbd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="31bbd-102">SYNOPSIS</span></span>
<span data-ttu-id="31bbd-103">在 SQL 集區上設定進一級的威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="31bbd-103">Sets a advanced threat protection settings on a SQL pool.</span></span>

## <span data-ttu-id="31bbd-104">語法</span><span class="sxs-lookup"><span data-stu-id="31bbd-104">SYNTAX</span></span>

### <span data-ttu-id="31bbd-105">UpdateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="31bbd-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>]
 [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31bbd-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="31bbd-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31bbd-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="31bbd-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31bbd-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="31bbd-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31bbd-109">描述</span><span class="sxs-lookup"><span data-stu-id="31bbd-109">DESCRIPTION</span></span>
<span data-ttu-id="31bbd-110">**Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting** Cmdlet 在 Azure Synapse Analytics SQL 集區上設定進一代威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="31bbd-110">The **Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure Synapse Analytics SQL pool.</span></span>
<span data-ttu-id="31bbd-111">若要在 SQL 資料庫上啟用進位威脅防護，必須在該 SQL 資料庫上啟用稽核設定。</span><span class="sxs-lookup"><span data-stu-id="31bbd-111">In order to enable advanced threat protection on a SQL pool an auditing settings must be enabled on that SQL pool.</span></span>

## <span data-ttu-id="31bbd-112">例子</span><span class="sxs-lookup"><span data-stu-id="31bbd-112">EXAMPLES</span></span>

### <span data-ttu-id="31bbd-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="31bbd-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="31bbd-114">此命令會針對名為 ContosoWorkspace 的工作區下名為 ContosoSqlPool 的 SQL 集區設定進一步威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="31bbd-114">This command sets the advanced threat protection settings for a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="31bbd-115">參數</span><span class="sxs-lookup"><span data-stu-id="31bbd-115">PARAMETERS</span></span>

### <span data-ttu-id="31bbd-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="31bbd-116">-AsJob</span></span>
<span data-ttu-id="31bbd-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="31bbd-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="31bbd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31bbd-118">-DefaultProfile</span></span>
<span data-ttu-id="31bbd-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="31bbd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31bbd-120">-EmailAdmin</span><span class="sxs-lookup"><span data-stu-id="31bbd-120">-EmailAdmin</span></span>
<span data-ttu-id="31bbd-121">定義是否要將電子郵件給系統管理員。</span><span class="sxs-lookup"><span data-stu-id="31bbd-121">Defines whether to email administrators.</span></span>

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

### <span data-ttu-id="31bbd-122">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="31bbd-122">-ExcludedDetectionType</span></span>
<span data-ttu-id="31bbd-123">要排除的偵測類型。</span><span class="sxs-lookup"><span data-stu-id="31bbd-123">Detection types to exclude.</span></span>

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

### <span data-ttu-id="31bbd-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31bbd-124">-InputObject</span></span>
<span data-ttu-id="31bbd-125">SQL 資料庫輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="31bbd-125">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="31bbd-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="31bbd-126">-Name</span></span>
<span data-ttu-id="31bbd-127">Synapse SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="31bbd-127">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="31bbd-128">-NotificationRecipientsEmail</span><span class="sxs-lookup"><span data-stu-id="31bbd-128">-NotificationRecipientsEmail</span></span>
<span data-ttu-id="31bbd-129">這是要傳送通知之電子郵件地址的分號分隔清單。</span><span class="sxs-lookup"><span data-stu-id="31bbd-129">A semicolon separated list of email addresses to send the alerts to.</span></span>

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

### <span data-ttu-id="31bbd-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31bbd-130">-ResourceGroupName</span></span>
<span data-ttu-id="31bbd-131">資源組名。</span><span class="sxs-lookup"><span data-stu-id="31bbd-131">Resource group name.</span></span>

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

### <span data-ttu-id="31bbd-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31bbd-132">-ResourceId</span></span>
<span data-ttu-id="31bbd-133">Synapse SQL Pool 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="31bbd-133">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="31bbd-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="31bbd-134">-RetentionInDays</span></span>
<span data-ttu-id="31bbd-135">稽核記錄保留天數。</span><span class="sxs-lookup"><span data-stu-id="31bbd-135">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="31bbd-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="31bbd-136">-StorageAccountName</span></span>
<span data-ttu-id="31bbd-137">儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="31bbd-137">The name of the storage account.</span></span>

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

### <span data-ttu-id="31bbd-138">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="31bbd-138">-WorkspaceName</span></span>
<span data-ttu-id="31bbd-139">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="31bbd-139">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="31bbd-140">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="31bbd-140">-WorkspaceObject</span></span>
<span data-ttu-id="31bbd-141">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="31bbd-141">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="31bbd-142">-確認</span><span class="sxs-lookup"><span data-stu-id="31bbd-142">-Confirm</span></span>
<span data-ttu-id="31bbd-143">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="31bbd-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31bbd-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31bbd-144">-WhatIf</span></span>
<span data-ttu-id="31bbd-145">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="31bbd-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31bbd-146">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="31bbd-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31bbd-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31bbd-147">CommonParameters</span></span>
<span data-ttu-id="31bbd-148">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="31bbd-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31bbd-149">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="31bbd-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31bbd-150">輸入</span><span class="sxs-lookup"><span data-stu-id="31bbd-150">INPUTS</span></span>

### <span data-ttu-id="31bbd-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="31bbd-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="31bbd-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="31bbd-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="31bbd-153">輸出</span><span class="sxs-lookup"><span data-stu-id="31bbd-153">OUTPUTS</span></span>

### <span data-ttu-id="31bbd-154">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="31bbd-154">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span></span>

## <span data-ttu-id="31bbd-155">筆記</span><span class="sxs-lookup"><span data-stu-id="31bbd-155">NOTES</span></span>

## <span data-ttu-id="31bbd-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="31bbd-156">RELATED LINKS</span></span>
