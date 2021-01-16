---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 4fb27d1d822d72de9564e9acc900122016940c6d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276796"
---
# <span data-ttu-id="1cc20-101">Update-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="1cc20-101">Update-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="1cc20-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1cc20-102">SYNOPSIS</span></span>
<span data-ttu-id="1cc20-103">更新工作區上的「高級威脅防護」設定。</span><span class="sxs-lookup"><span data-stu-id="1cc20-103">Updates an advanced threat protection settings on a workspace.</span></span>

## <span data-ttu-id="1cc20-104">句法</span><span class="sxs-lookup"><span data-stu-id="1cc20-104">SYNTAX</span></span>

### <span data-ttu-id="1cc20-105">UpdateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1cc20-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cc20-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cc20-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cc20-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cc20-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-NotificationRecipientsEmail <String>]
 [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1cc20-108">說明</span><span class="sxs-lookup"><span data-stu-id="1cc20-108">DESCRIPTION</span></span>
<span data-ttu-id="1cc20-109">**AzSynapseSqlAdvancedThreatProtectionSetting** Cmdlet 會更新 Azure Synapse Analytics 工作區上的高級威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="1cc20-109">The **Update-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet updates an advanced threat protection settings on an Azure Synapse Analytics Workspace.</span></span> <span data-ttu-id="1cc20-110">若要在工作區上啟用高級威脅防護，必須在該工作區啟用 [審核] 設定。</span><span class="sxs-lookup"><span data-stu-id="1cc20-110">In order to enable advanced threat protection on a workspace an auditing settings must be enabled on that workspace.</span></span>

## <span data-ttu-id="1cc20-111">示例</span><span class="sxs-lookup"><span data-stu-id="1cc20-111">EXAMPLES</span></span>

### <span data-ttu-id="1cc20-112">範例1</span><span class="sxs-lookup"><span data-stu-id="1cc20-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -NotificationRecipientsEmail "admin01@contoso.com;secadmin@contoso.com" -EmailAdmin $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="1cc20-113">這個命令會更新名為 ContosoWorkspace 的工作區的高級威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="1cc20-113">This command updates the advanced threat protection settings for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="1cc20-114">參數</span><span class="sxs-lookup"><span data-stu-id="1cc20-114">PARAMETERS</span></span>

### <span data-ttu-id="1cc20-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1cc20-115">-AsJob</span></span>
<span data-ttu-id="1cc20-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1cc20-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1cc20-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cc20-117">-DefaultProfile</span></span>
<span data-ttu-id="1cc20-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1cc20-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cc20-119">-EmailAdmin</span><span class="sxs-lookup"><span data-stu-id="1cc20-119">-EmailAdmin</span></span>
<span data-ttu-id="1cc20-120">定義是否要傳送電子郵件給系統管理員。</span><span class="sxs-lookup"><span data-stu-id="1cc20-120">Defines whether to email administrators.</span></span>

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

### <span data-ttu-id="1cc20-121">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="1cc20-121">-ExcludedDetectionType</span></span>
<span data-ttu-id="1cc20-122">要排除的偵測類型。</span><span class="sxs-lookup"><span data-stu-id="1cc20-122">Detection types to exclude.</span></span>

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

### <span data-ttu-id="1cc20-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1cc20-123">-InputObject</span></span>
<span data-ttu-id="1cc20-124">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="1cc20-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="1cc20-125">-NotificationRecipientsEmail</span><span class="sxs-lookup"><span data-stu-id="1cc20-125">-NotificationRecipientsEmail</span></span>
<span data-ttu-id="1cc20-126">要傳送提醒的電子郵件地址清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="1cc20-126">A semicolon separated list of email addresses to send the alerts to.</span></span>

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

### <span data-ttu-id="1cc20-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cc20-127">-ResourceGroupName</span></span>
<span data-ttu-id="1cc20-128">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="1cc20-128">Resource group name.</span></span>

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

### <span data-ttu-id="1cc20-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1cc20-129">-ResourceId</span></span>
<span data-ttu-id="1cc20-130">Synapse 工作區的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1cc20-130">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="1cc20-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="1cc20-131">-RetentionInDays</span></span>
<span data-ttu-id="1cc20-132">審計記錄的保留天數。</span><span class="sxs-lookup"><span data-stu-id="1cc20-132">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="1cc20-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1cc20-133">-StorageAccountName</span></span>
<span data-ttu-id="1cc20-134">儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="1cc20-134">The name of the storage account.</span></span>

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

### <span data-ttu-id="1cc20-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1cc20-135">-WorkspaceName</span></span>
<span data-ttu-id="1cc20-136">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="1cc20-136">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="1cc20-137">-確認</span><span class="sxs-lookup"><span data-stu-id="1cc20-137">-Confirm</span></span>
<span data-ttu-id="1cc20-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1cc20-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cc20-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cc20-139">-WhatIf</span></span>
<span data-ttu-id="1cc20-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1cc20-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cc20-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1cc20-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cc20-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cc20-142">CommonParameters</span></span>
<span data-ttu-id="1cc20-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1cc20-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cc20-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1cc20-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cc20-145">輸入</span><span class="sxs-lookup"><span data-stu-id="1cc20-145">INPUTS</span></span>

### <span data-ttu-id="1cc20-146">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="1cc20-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="1cc20-147">輸出</span><span class="sxs-lookup"><span data-stu-id="1cc20-147">OUTPUTS</span></span>

### <span data-ttu-id="1cc20-148">PSServerSecurityAlertPolicy 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="1cc20-148">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span></span>

## <span data-ttu-id="1cc20-149">筆記</span><span class="sxs-lookup"><span data-stu-id="1cc20-149">NOTES</span></span>

## <span data-ttu-id="1cc20-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="1cc20-150">RELATED LINKS</span></span>
