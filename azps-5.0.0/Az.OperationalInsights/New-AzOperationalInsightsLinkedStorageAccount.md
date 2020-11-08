---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 1293a2d045da5da1856052495516e9311e42e5f2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139527"
---
# <span data-ttu-id="7eb00-101">New-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7eb00-101">New-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="7eb00-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7eb00-102">SYNOPSIS</span></span>
<span data-ttu-id="7eb00-103">建立工作區的連結儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="7eb00-103">Create linked storage account for workspace</span></span>

## <span data-ttu-id="7eb00-104">句法</span><span class="sxs-lookup"><span data-stu-id="7eb00-104">SYNTAX</span></span>

```
New-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DataSourceType] <String> [-StorageAccountIds] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7eb00-105">說明</span><span class="sxs-lookup"><span data-stu-id="7eb00-105">DESCRIPTION</span></span>
<span data-ttu-id="7eb00-106">建立工作區的連結儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="7eb00-106">Create linked storage account for workspace</span></span>

## <span data-ttu-id="7eb00-107">示例</span><span class="sxs-lookup"><span data-stu-id="7eb00-107">EXAMPLES</span></span>

### <span data-ttu-id="7eb00-108">範例1</span><span class="sxs-lookup"><span data-stu-id="7eb00-108">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName {rg-name} -Name {account-name}

New-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs -StorageAccountIds $account.Id

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/CustomLogs
Name              : customlogs
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{storage-account}}
```

<span data-ttu-id="7eb00-109">新增工作區的連結儲存空間</span><span class="sxs-lookup"><span data-stu-id="7eb00-109">Add linked storage for workspace</span></span>

## <span data-ttu-id="7eb00-110">參數</span><span class="sxs-lookup"><span data-stu-id="7eb00-110">PARAMETERS</span></span>

### <span data-ttu-id="7eb00-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="7eb00-111">-DataSourceType</span></span>
<span data-ttu-id="7eb00-112">資料來源類型應該是 "CustomLogs"、"AzureWatson"。</span><span class="sxs-lookup"><span data-stu-id="7eb00-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="7eb00-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eb00-113">-DefaultProfile</span></span>
<span data-ttu-id="7eb00-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7eb00-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7eb00-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7eb00-115">-Force</span></span>
<span data-ttu-id="7eb00-116">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="7eb00-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="7eb00-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7eb00-117">-ResourceGroupName</span></span>
<span data-ttu-id="7eb00-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7eb00-118">The resource group name.</span></span>

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

### <span data-ttu-id="7eb00-119">-StorageAccountIds</span><span class="sxs-lookup"><span data-stu-id="7eb00-119">-StorageAccountIds</span></span>
<span data-ttu-id="7eb00-120">儲存空間帳戶識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="7eb00-120">list of storage account Id.</span></span>

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

### <span data-ttu-id="7eb00-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7eb00-121">-WorkspaceName</span></span>
<span data-ttu-id="7eb00-122">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="7eb00-122">The workspace name.</span></span>

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

### <span data-ttu-id="7eb00-123">-確認</span><span class="sxs-lookup"><span data-stu-id="7eb00-123">-Confirm</span></span>
<span data-ttu-id="7eb00-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7eb00-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7eb00-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7eb00-125">-WhatIf</span></span>
<span data-ttu-id="7eb00-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7eb00-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7eb00-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7eb00-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7eb00-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eb00-128">CommonParameters</span></span>
<span data-ttu-id="7eb00-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7eb00-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eb00-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7eb00-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eb00-131">輸入</span><span class="sxs-lookup"><span data-stu-id="7eb00-131">INPUTS</span></span>

### <span data-ttu-id="7eb00-132">System.object</span><span class="sxs-lookup"><span data-stu-id="7eb00-132">System.String</span></span>

## <span data-ttu-id="7eb00-133">輸出</span><span class="sxs-lookup"><span data-stu-id="7eb00-133">OUTPUTS</span></span>

### <span data-ttu-id="7eb00-134">PSLinkedStorageAccountsResource 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="7eb00-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="7eb00-135">筆記</span><span class="sxs-lookup"><span data-stu-id="7eb00-135">NOTES</span></span>

## <span data-ttu-id="7eb00-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="7eb00-136">RELATED LINKS</span></span>