---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: B4EC9132-8DB9-498D-8B3F-2AB51D8EA03A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightsazureactivitylogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsAzureActivityLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsAzureActivityLogDataSource.md
ms.openlocfilehash: 6b3009a37a314b70d258f597823f8da062970450
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447017"
---
# <span data-ttu-id="3f4f2-101">New-AzureRmOperationalInsightsAzureActivityLogDataSource</span><span class="sxs-lookup"><span data-stu-id="3f4f2-101">New-AzureRmOperationalInsightsAzureActivityLogDataSource</span></span>

## <span data-ttu-id="3f4f2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3f4f2-102">SYNOPSIS</span></span>
<span data-ttu-id="3f4f2-103">從指定的訂閱收集 Azure 活動記錄。</span><span class="sxs-lookup"><span data-stu-id="3f4f2-103">Collect Azure Activity log from given subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f4f2-104">句法</span><span class="sxs-lookup"><span data-stu-id="3f4f2-104">SYNTAX</span></span>

### <span data-ttu-id="3f4f2-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="3f4f2-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsAzureActivityLogDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f4f2-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3f4f2-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsAzureActivityLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f4f2-107">說明</span><span class="sxs-lookup"><span data-stu-id="3f4f2-107">DESCRIPTION</span></span>
<span data-ttu-id="3f4f2-108">New-AzureRmOperationalInsightsAzureActivityLogDataSource 啟用 Log Analytics 以從指定的訂閱收集 Azure 活動記錄。</span><span class="sxs-lookup"><span data-stu-id="3f4f2-108">The New-AzureRmOperationalInsightsAzureActivityLogDataSource enable Log Analytics to collect Azure activity log from given subscription.</span></span>

## <span data-ttu-id="3f4f2-109">示例</span><span class="sxs-lookup"><span data-stu-id="3f4f2-109">EXAMPLES</span></span>

### <span data-ttu-id="3f4f2-110">範例1</span><span class="sxs-lookup"><span data-stu-id="3f4f2-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="3f4f2-111">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="3f4f2-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="3f4f2-112">參數</span><span class="sxs-lookup"><span data-stu-id="3f4f2-112">PARAMETERS</span></span>

### <span data-ttu-id="3f4f2-113">-BackfillStartTime</span><span class="sxs-lookup"><span data-stu-id="3f4f2-113">-BackfillStartTime</span></span>
<span data-ttu-id="3f4f2-114">您可以選擇從一周之前回填記錄。</span><span class="sxs-lookup"><span data-stu-id="3f4f2-114">You can choose to backfill logs from a week ago.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f4f2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f4f2-115">-DefaultProfile</span></span>
<span data-ttu-id="3f4f2-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3f4f2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f4f2-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3f4f2-117">-Force</span></span>
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

### <span data-ttu-id="3f4f2-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="3f4f2-118">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f4f2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f4f2-119">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f4f2-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3f4f2-120">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f4f2-121">-工作區</span><span class="sxs-lookup"><span data-stu-id="3f4f2-121">-Workspace</span></span>
```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f4f2-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3f4f2-122">-WorkspaceName</span></span>
```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f4f2-123">-確認</span><span class="sxs-lookup"><span data-stu-id="3f4f2-123">-Confirm</span></span>
<span data-ttu-id="3f4f2-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3f4f2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f4f2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f4f2-125">-WhatIf</span></span>
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

### <span data-ttu-id="3f4f2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f4f2-126">CommonParameters</span></span>
<span data-ttu-id="3f4f2-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3f4f2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f4f2-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3f4f2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f4f2-129">輸入</span><span class="sxs-lookup"><span data-stu-id="3f4f2-129">INPUTS</span></span>

### <span data-ttu-id="3f4f2-130">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="3f4f2-130">PSWorkspace</span></span>
<span data-ttu-id="3f4f2-131">形參 "Workspace" 接受管線中類型 ' PSWorkspace」的值</span><span class="sxs-lookup"><span data-stu-id="3f4f2-131">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="3f4f2-132">輸出</span><span class="sxs-lookup"><span data-stu-id="3f4f2-132">OUTPUTS</span></span>

### <span data-ttu-id="3f4f2-133">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="3f4f2-133">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="3f4f2-134">筆記</span><span class="sxs-lookup"><span data-stu-id="3f4f2-134">NOTES</span></span>

## <span data-ttu-id="3f4f2-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="3f4f2-135">RELATED LINKS</span></span>

