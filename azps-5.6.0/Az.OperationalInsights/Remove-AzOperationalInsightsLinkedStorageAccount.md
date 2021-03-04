---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 8e4dd13b93a0aadf8c69325bc6d79a2a1b3e1359
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911562"
---
# <span data-ttu-id="a5cf5-101">Remove-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a5cf5-101">Remove-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="a5cf5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a5cf5-102">SYNOPSIS</span></span>
<span data-ttu-id="a5cf5-103">刪除工作區的連結儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="a5cf5-103">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="a5cf5-104">語法</span><span class="sxs-lookup"><span data-stu-id="a5cf5-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5cf5-105">描述</span><span class="sxs-lookup"><span data-stu-id="a5cf5-105">DESCRIPTION</span></span>
<span data-ttu-id="a5cf5-106">刪除工作區的連結儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="a5cf5-106">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="a5cf5-107">例子</span><span class="sxs-lookup"><span data-stu-id="a5cf5-107">EXAMPLES</span></span>

### <span data-ttu-id="a5cf5-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="a5cf5-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs
True
```

<span data-ttu-id="a5cf5-109">刪除 {workspace-name} 類型為 "CustomLogs" 的連結儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="a5cf5-109">Delete linked storage account with type "CustomLogs" for {workspace-name}</span></span>

## <span data-ttu-id="a5cf5-110">參數</span><span class="sxs-lookup"><span data-stu-id="a5cf5-110">PARAMETERS</span></span>

### <span data-ttu-id="a5cf5-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="a5cf5-111">-DataSourceType</span></span>
<span data-ttu-id="a5cf5-112">資料來源類型應該是其中一個'CustomLogs'，'AzureWatson'。</span><span class="sxs-lookup"><span data-stu-id="a5cf5-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CustomLogs, AzureWatson

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5cf5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5cf5-113">-DefaultProfile</span></span>
<span data-ttu-id="a5cf5-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a5cf5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5cf5-115">-強制</span><span class="sxs-lookup"><span data-stu-id="a5cf5-115">-Force</span></span>
<span data-ttu-id="a5cf5-116">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="a5cf5-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="a5cf5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5cf5-117">-ResourceGroupName</span></span>
<span data-ttu-id="a5cf5-118">資源組名。</span><span class="sxs-lookup"><span data-stu-id="a5cf5-118">The resource group name.</span></span>

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

### <span data-ttu-id="a5cf5-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a5cf5-119">-WorkspaceName</span></span>
<span data-ttu-id="a5cf5-120">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="a5cf5-120">The workspace name.</span></span>

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

### <span data-ttu-id="a5cf5-121">-確認</span><span class="sxs-lookup"><span data-stu-id="a5cf5-121">-Confirm</span></span>
<span data-ttu-id="a5cf5-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a5cf5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5cf5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5cf5-123">-WhatIf</span></span>
<span data-ttu-id="a5cf5-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a5cf5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5cf5-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a5cf5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5cf5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5cf5-126">CommonParameters</span></span>
<span data-ttu-id="a5cf5-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a5cf5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5cf5-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5cf5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5cf5-129">輸入</span><span class="sxs-lookup"><span data-stu-id="a5cf5-129">INPUTS</span></span>

### <span data-ttu-id="a5cf5-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a5cf5-130">System.String</span></span>

## <span data-ttu-id="a5cf5-131">輸出</span><span class="sxs-lookup"><span data-stu-id="a5cf5-131">OUTPUTS</span></span>

### <span data-ttu-id="a5cf5-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a5cf5-132">System.Boolean</span></span>

## <span data-ttu-id="a5cf5-133">筆記</span><span class="sxs-lookup"><span data-stu-id="a5cf5-133">NOTES</span></span>

## <span data-ttu-id="a5cf5-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="a5cf5-134">RELATED LINKS</span></span>
