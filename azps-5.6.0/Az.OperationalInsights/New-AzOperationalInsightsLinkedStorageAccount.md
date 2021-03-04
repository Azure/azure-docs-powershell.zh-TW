---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: f1b920c3a67865cbed66c15bc686e3e38e3562db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908373"
---
# <span data-ttu-id="fcdae-101">New-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fcdae-101">New-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="fcdae-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fcdae-102">SYNOPSIS</span></span>
<span data-ttu-id="fcdae-103">建立工作區的連結儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="fcdae-103">Create linked storage account for workspace</span></span>

## <span data-ttu-id="fcdae-104">語法</span><span class="sxs-lookup"><span data-stu-id="fcdae-104">SYNTAX</span></span>

```
New-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DataSourceType] <String> [-StorageAccountIds] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcdae-105">描述</span><span class="sxs-lookup"><span data-stu-id="fcdae-105">DESCRIPTION</span></span>
<span data-ttu-id="fcdae-106">建立工作區的連結儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="fcdae-106">Create linked storage account for workspace</span></span>

## <span data-ttu-id="fcdae-107">例子</span><span class="sxs-lookup"><span data-stu-id="fcdae-107">EXAMPLES</span></span>

### <span data-ttu-id="fcdae-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="fcdae-108">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName {rg-name} -Name {account-name}

New-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs -StorageAccountIds $account.Id

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/CustomLogs
Name              : customlogs
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{storage-account}}
```

<span data-ttu-id="fcdae-109">新增工作區的連結儲存空間</span><span class="sxs-lookup"><span data-stu-id="fcdae-109">Add linked storage for workspace</span></span>

## <span data-ttu-id="fcdae-110">參數</span><span class="sxs-lookup"><span data-stu-id="fcdae-110">PARAMETERS</span></span>

### <span data-ttu-id="fcdae-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="fcdae-111">-DataSourceType</span></span>
<span data-ttu-id="fcdae-112">資料來源類型應該是其中一個'CustomLogs'，'AzureWatson'。</span><span class="sxs-lookup"><span data-stu-id="fcdae-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="fcdae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcdae-113">-DefaultProfile</span></span>
<span data-ttu-id="fcdae-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fcdae-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcdae-115">-強制</span><span class="sxs-lookup"><span data-stu-id="fcdae-115">-Force</span></span>
<span data-ttu-id="fcdae-116">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="fcdae-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="fcdae-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcdae-117">-ResourceGroupName</span></span>
<span data-ttu-id="fcdae-118">資源組名。</span><span class="sxs-lookup"><span data-stu-id="fcdae-118">The resource group name.</span></span>

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

### <span data-ttu-id="fcdae-119">-StorageAccountIds</span><span class="sxs-lookup"><span data-stu-id="fcdae-119">-StorageAccountIds</span></span>
<span data-ttu-id="fcdae-120">儲存空間帳戶識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="fcdae-120">list of storage account Id.</span></span>

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

### <span data-ttu-id="fcdae-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fcdae-121">-WorkspaceName</span></span>
<span data-ttu-id="fcdae-122">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="fcdae-122">The workspace name.</span></span>

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

### <span data-ttu-id="fcdae-123">-確認</span><span class="sxs-lookup"><span data-stu-id="fcdae-123">-Confirm</span></span>
<span data-ttu-id="fcdae-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="fcdae-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcdae-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcdae-125">-WhatIf</span></span>
<span data-ttu-id="fcdae-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fcdae-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcdae-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fcdae-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcdae-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcdae-128">CommonParameters</span></span>
<span data-ttu-id="fcdae-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fcdae-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcdae-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fcdae-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcdae-131">輸入</span><span class="sxs-lookup"><span data-stu-id="fcdae-131">INPUTS</span></span>

### <span data-ttu-id="fcdae-132">System.String</span><span class="sxs-lookup"><span data-stu-id="fcdae-132">System.String</span></span>

## <span data-ttu-id="fcdae-133">輸出</span><span class="sxs-lookup"><span data-stu-id="fcdae-133">OUTPUTS</span></span>

### <span data-ttu-id="fcdae-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="fcdae-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="fcdae-135">筆記</span><span class="sxs-lookup"><span data-stu-id="fcdae-135">NOTES</span></span>

## <span data-ttu-id="fcdae-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="fcdae-136">RELATED LINKS</span></span>
