---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 26B1921E-6052-471B-B5B6-F2853536A425
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/enable-azoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsIISLogCollection.md
ms.openlocfilehash: 6257762d5b0042635645533cf610132a3e12fd27
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913790"
---
# <span data-ttu-id="01f09-101">Enable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="01f09-101">Enable-AzOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="01f09-102">簡介</span><span class="sxs-lookup"><span data-stu-id="01f09-102">SYNOPSIS</span></span>
<span data-ttu-id="01f09-103">從工作區中的電腦開始收集 IIS 記錄。</span><span class="sxs-lookup"><span data-stu-id="01f09-103">Starts collection of IIS logs from computers in a workspace.</span></span>

## <span data-ttu-id="01f09-104">語法</span><span class="sxs-lookup"><span data-stu-id="01f09-104">SYNTAX</span></span>

### <span data-ttu-id="01f09-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="01f09-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01f09-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="01f09-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01f09-107">描述</span><span class="sxs-lookup"><span data-stu-id="01f09-107">DESCRIPTION</span></span>
<span data-ttu-id="01f09-108">**Enable-AzOperationalInsightsIISLogCollection** Cmdlet 會從工作區中連接的電腦開始收集網際網路資訊服務 (IIS) 記錄。</span><span class="sxs-lookup"><span data-stu-id="01f09-108">The **Enable-AzOperationalInsightsIISLogCollection** cmdlet starts collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="01f09-109">例子</span><span class="sxs-lookup"><span data-stu-id="01f09-109">EXAMPLES</span></span>

## <span data-ttu-id="01f09-110">參數</span><span class="sxs-lookup"><span data-stu-id="01f09-110">PARAMETERS</span></span>

### <span data-ttu-id="01f09-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01f09-111">-DefaultProfile</span></span>
<span data-ttu-id="01f09-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="01f09-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01f09-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01f09-113">-ResourceGroupName</span></span>
<span data-ttu-id="01f09-114">指定包含電腦的資源組名。</span><span class="sxs-lookup"><span data-stu-id="01f09-114">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01f09-115">-工作區</span><span class="sxs-lookup"><span data-stu-id="01f09-115">-Workspace</span></span>
<span data-ttu-id="01f09-116">指定此 Cmdlet 在哪個工作區中操作。</span><span class="sxs-lookup"><span data-stu-id="01f09-116">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01f09-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="01f09-117">-WorkspaceName</span></span>
<span data-ttu-id="01f09-118">指定此 Cmdlet 操作之工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="01f09-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01f09-119">-確認</span><span class="sxs-lookup"><span data-stu-id="01f09-119">-Confirm</span></span>
<span data-ttu-id="01f09-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="01f09-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01f09-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01f09-121">-WhatIf</span></span>
<span data-ttu-id="01f09-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="01f09-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01f09-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="01f09-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01f09-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01f09-124">CommonParameters</span></span>
<span data-ttu-id="01f09-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="01f09-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01f09-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="01f09-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01f09-127">輸入</span><span class="sxs-lookup"><span data-stu-id="01f09-127">INPUTS</span></span>

### <span data-ttu-id="01f09-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="01f09-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="01f09-129">System.String</span><span class="sxs-lookup"><span data-stu-id="01f09-129">System.String</span></span>

## <span data-ttu-id="01f09-130">輸出</span><span class="sxs-lookup"><span data-stu-id="01f09-130">OUTPUTS</span></span>

### <span data-ttu-id="01f09-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="01f09-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="01f09-132">筆記</span><span class="sxs-lookup"><span data-stu-id="01f09-132">NOTES</span></span>

## <span data-ttu-id="01f09-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="01f09-133">RELATED LINKS</span></span>

[<span data-ttu-id="01f09-134">Disable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="01f09-134">Disable-AzOperationalInsightsIISLogCollection</span></span>](./Disable-AzOperationalInsightsIISLogCollection.md)


