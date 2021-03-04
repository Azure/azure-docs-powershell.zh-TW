---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 5766c93ba1fa7434b6ebd41f0c414f5e8a9a5073
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912170"
---
# <span data-ttu-id="8f937-101">Update-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="8f937-101">Update-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="8f937-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8f937-102">SYNOPSIS</span></span>
<span data-ttu-id="8f937-103">更新工作區上的進一威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="8f937-103">Updates an advanced threat protection settings on a workspace.</span></span>

## <span data-ttu-id="8f937-104">語法</span><span class="sxs-lookup"><span data-stu-id="8f937-104">SYNTAX</span></span>

### <span data-ttu-id="8f937-105">UpdateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8f937-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f937-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f937-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f937-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f937-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-NotificationRecipientsEmail <String>]
 [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8f937-108">描述</span><span class="sxs-lookup"><span data-stu-id="8f937-108">DESCRIPTION</span></span>
<span data-ttu-id="8f937-109">**Update-AzSynapseSqlAdvancedThreatProtectionSetting** Cmdlet 會更新 Azure Synapse Analytics Workspace 上的進一代威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="8f937-109">The **Update-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet updates an advanced threat protection settings on an Azure Synapse Analytics Workspace.</span></span> <span data-ttu-id="8f937-110">若要在工作區上啟用進位威脅防護，必須在該工作區上啟用稽核設定。</span><span class="sxs-lookup"><span data-stu-id="8f937-110">In order to enable advanced threat protection on a workspace an auditing settings must be enabled on that workspace.</span></span>

## <span data-ttu-id="8f937-111">例子</span><span class="sxs-lookup"><span data-stu-id="8f937-111">EXAMPLES</span></span>

### <span data-ttu-id="8f937-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="8f937-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -NotificationRecipientsEmail "admin01@contoso.com;secadmin@contoso.com" -EmailAdmin $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="8f937-113">此命令會更新名為 ContosoWorkspace 之工作區的進位威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="8f937-113">This command updates the advanced threat protection settings for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="8f937-114">參數</span><span class="sxs-lookup"><span data-stu-id="8f937-114">PARAMETERS</span></span>

### <span data-ttu-id="8f937-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f937-115">-AsJob</span></span>
<span data-ttu-id="8f937-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8f937-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8f937-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f937-117">-DefaultProfile</span></span>
<span data-ttu-id="8f937-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8f937-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f937-119">-EmailAdmin</span><span class="sxs-lookup"><span data-stu-id="8f937-119">-EmailAdmin</span></span>
<span data-ttu-id="8f937-120">定義是否要將電子郵件給系統管理員。</span><span class="sxs-lookup"><span data-stu-id="8f937-120">Defines whether to email administrators.</span></span>

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

### <span data-ttu-id="8f937-121">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="8f937-121">-ExcludedDetectionType</span></span>
<span data-ttu-id="8f937-122">要排除的偵測類型。</span><span class="sxs-lookup"><span data-stu-id="8f937-122">Detection types to exclude.</span></span>

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

### <span data-ttu-id="8f937-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f937-123">-InputObject</span></span>
<span data-ttu-id="8f937-124">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="8f937-124">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f937-125">-NotificationRecipientsEmail</span><span class="sxs-lookup"><span data-stu-id="8f937-125">-NotificationRecipientsEmail</span></span>
<span data-ttu-id="8f937-126">這是要傳送通知之電子郵件地址的分號分隔清單。</span><span class="sxs-lookup"><span data-stu-id="8f937-126">A semicolon separated list of email addresses to send the alerts to.</span></span>

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

### <span data-ttu-id="8f937-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f937-127">-ResourceGroupName</span></span>
<span data-ttu-id="8f937-128">資源組名。</span><span class="sxs-lookup"><span data-stu-id="8f937-128">Resource group name.</span></span>

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

### <span data-ttu-id="8f937-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f937-129">-ResourceId</span></span>
<span data-ttu-id="8f937-130">Synapse 工作區的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8f937-130">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="8f937-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="8f937-131">-RetentionInDays</span></span>
<span data-ttu-id="8f937-132">稽核記錄保留天數。</span><span class="sxs-lookup"><span data-stu-id="8f937-132">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="8f937-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8f937-133">-StorageAccountName</span></span>
<span data-ttu-id="8f937-134">儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f937-134">The name of the storage account.</span></span>

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

### <span data-ttu-id="8f937-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8f937-135">-WorkspaceName</span></span>
<span data-ttu-id="8f937-136">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f937-136">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8f937-137">-確認</span><span class="sxs-lookup"><span data-stu-id="8f937-137">-Confirm</span></span>
<span data-ttu-id="8f937-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8f937-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f937-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f937-139">-WhatIf</span></span>
<span data-ttu-id="8f937-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8f937-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f937-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8f937-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f937-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f937-142">CommonParameters</span></span>
<span data-ttu-id="8f937-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8f937-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f937-144">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f937-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f937-145">輸入</span><span class="sxs-lookup"><span data-stu-id="8f937-145">INPUTS</span></span>

### <span data-ttu-id="8f937-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8f937-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="8f937-147">輸出</span><span class="sxs-lookup"><span data-stu-id="8f937-147">OUTPUTS</span></span>

### <span data-ttu-id="8f937-148">Microsoft.Azure.Commands.Synapse.models.PSServerSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="8f937-148">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span></span>

## <span data-ttu-id="8f937-149">筆記</span><span class="sxs-lookup"><span data-stu-id="8f937-149">NOTES</span></span>

## <span data-ttu-id="8f937-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="8f937-150">RELATED LINKS</span></span>
