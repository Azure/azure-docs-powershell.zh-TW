---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: b6e57494daf556c3b824ee06735711042d3851b9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98286752"
---
# <span data-ttu-id="bce74-101">Set-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bce74-101">Set-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="bce74-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bce74-102">SYNOPSIS</span></span>
<span data-ttu-id="bce74-103">針對工作區設定連結儲存帳戶</span><span class="sxs-lookup"><span data-stu-id="bce74-103">Set linked storage account for workspace</span></span>

## <span data-ttu-id="bce74-104">句法</span><span class="sxs-lookup"><span data-stu-id="bce74-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DataSourceType] <String> [-StorageAccountIds] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bce74-105">說明</span><span class="sxs-lookup"><span data-stu-id="bce74-105">DESCRIPTION</span></span>
<span data-ttu-id="bce74-106">針對工作區設定連結儲存帳戶</span><span class="sxs-lookup"><span data-stu-id="bce74-106">Set linked storage account for workspace</span></span>

## <span data-ttu-id="bce74-107">示例</span><span class="sxs-lookup"><span data-stu-id="bce74-107">EXAMPLES</span></span>

### <span data-ttu-id="bce74-108">範例1</span><span class="sxs-lookup"><span data-stu-id="bce74-108">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName {rg-name} -Name {account-name}

Set-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs -StorageAccountIds $account.Id

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/CustomLogs
Name              : customlogs
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{storage-account}}
```

<span data-ttu-id="bce74-109">設定工作區的連結儲存</span><span class="sxs-lookup"><span data-stu-id="bce74-109">Set linked storage for workspace</span></span>

## <span data-ttu-id="bce74-110">參數</span><span class="sxs-lookup"><span data-stu-id="bce74-110">PARAMETERS</span></span>

### <span data-ttu-id="bce74-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="bce74-111">-DataSourceType</span></span>
<span data-ttu-id="bce74-112">資料來源類型應該是 "CustomLogs"、"AzureWatson"。</span><span class="sxs-lookup"><span data-stu-id="bce74-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CustomLogs, AzureWatson

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bce74-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bce74-113">-DefaultProfile</span></span>
<span data-ttu-id="bce74-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bce74-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bce74-115">-Force</span><span class="sxs-lookup"><span data-stu-id="bce74-115">-Force</span></span>
<span data-ttu-id="bce74-116">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="bce74-116">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bce74-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bce74-117">-ResourceGroupName</span></span>
<span data-ttu-id="bce74-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bce74-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bce74-119">-StorageAccountIds</span><span class="sxs-lookup"><span data-stu-id="bce74-119">-StorageAccountIds</span></span>
<span data-ttu-id="bce74-120">儲存空間帳戶識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="bce74-120">list of storage account Id.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bce74-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bce74-121">-WorkspaceName</span></span>
<span data-ttu-id="bce74-122">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="bce74-122">The workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bce74-123">-確認</span><span class="sxs-lookup"><span data-stu-id="bce74-123">-Confirm</span></span>
<span data-ttu-id="bce74-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bce74-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bce74-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bce74-125">-WhatIf</span></span>
<span data-ttu-id="bce74-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bce74-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bce74-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bce74-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bce74-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bce74-128">CommonParameters</span></span>
<span data-ttu-id="bce74-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bce74-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bce74-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bce74-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bce74-131">輸入</span><span class="sxs-lookup"><span data-stu-id="bce74-131">INPUTS</span></span>

### <span data-ttu-id="bce74-132">System.object</span><span class="sxs-lookup"><span data-stu-id="bce74-132">System.String</span></span>

## <span data-ttu-id="bce74-133">輸出</span><span class="sxs-lookup"><span data-stu-id="bce74-133">OUTPUTS</span></span>

### <span data-ttu-id="bce74-134">PSLinkedStorageAccountsResource 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="bce74-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="bce74-135">筆記</span><span class="sxs-lookup"><span data-stu-id="bce74-135">NOTES</span></span>

## <span data-ttu-id="bce74-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="bce74-136">RELATED LINKS</span></span>
