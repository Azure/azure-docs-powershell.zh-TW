---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 56f9f5b86e3e98ca9bba13604c3086d2189c45c5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435692"
---
# <span data-ttu-id="8533a-101">Remove-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8533a-101">Remove-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="8533a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8533a-102">SYNOPSIS</span></span>
<span data-ttu-id="8533a-103">刪除工作區的連結儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="8533a-103">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="8533a-104">句法</span><span class="sxs-lookup"><span data-stu-id="8533a-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8533a-105">說明</span><span class="sxs-lookup"><span data-stu-id="8533a-105">DESCRIPTION</span></span>
<span data-ttu-id="8533a-106">刪除工作區的連結儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="8533a-106">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="8533a-107">示例</span><span class="sxs-lookup"><span data-stu-id="8533a-107">EXAMPLES</span></span>

### <span data-ttu-id="8533a-108">範例1</span><span class="sxs-lookup"><span data-stu-id="8533a-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs
True
```

<span data-ttu-id="8533a-109">刪除 {工作區名稱} 類型為 "CustomLogs" 的連結儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="8533a-109">Delete linked storage account with type "CustomLogs" for {workspace-name}</span></span>

## <span data-ttu-id="8533a-110">參數</span><span class="sxs-lookup"><span data-stu-id="8533a-110">PARAMETERS</span></span>

### <span data-ttu-id="8533a-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="8533a-111">-DataSourceType</span></span>
<span data-ttu-id="8533a-112">資料來源類型應該是 "CustomLogs"、"AzureWatson"。</span><span class="sxs-lookup"><span data-stu-id="8533a-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="8533a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8533a-113">-DefaultProfile</span></span>
<span data-ttu-id="8533a-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8533a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8533a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8533a-115">-Force</span></span>
<span data-ttu-id="8533a-116">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="8533a-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="8533a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8533a-117">-ResourceGroupName</span></span>
<span data-ttu-id="8533a-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8533a-118">The resource group name.</span></span>

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

### <span data-ttu-id="8533a-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8533a-119">-WorkspaceName</span></span>
<span data-ttu-id="8533a-120">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="8533a-120">The workspace name.</span></span>

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

### <span data-ttu-id="8533a-121">-確認</span><span class="sxs-lookup"><span data-stu-id="8533a-121">-Confirm</span></span>
<span data-ttu-id="8533a-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8533a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8533a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8533a-123">-WhatIf</span></span>
<span data-ttu-id="8533a-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8533a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8533a-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8533a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8533a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8533a-126">CommonParameters</span></span>
<span data-ttu-id="8533a-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8533a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8533a-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8533a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8533a-129">輸入</span><span class="sxs-lookup"><span data-stu-id="8533a-129">INPUTS</span></span>

### <span data-ttu-id="8533a-130">System.object</span><span class="sxs-lookup"><span data-stu-id="8533a-130">System.String</span></span>

## <span data-ttu-id="8533a-131">輸出</span><span class="sxs-lookup"><span data-stu-id="8533a-131">OUTPUTS</span></span>

### <span data-ttu-id="8533a-132">System.object</span><span class="sxs-lookup"><span data-stu-id="8533a-132">System.Boolean</span></span>

## <span data-ttu-id="8533a-133">筆記</span><span class="sxs-lookup"><span data-stu-id="8533a-133">NOTES</span></span>

## <span data-ttu-id="8533a-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="8533a-134">RELATED LINKS</span></span>
