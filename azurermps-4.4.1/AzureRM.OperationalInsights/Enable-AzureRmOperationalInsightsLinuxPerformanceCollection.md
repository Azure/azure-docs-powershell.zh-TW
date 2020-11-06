---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 10141D75-B58D-42B0-B0A6-92FF630E534C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: 1ef047fa821a2eb74f0c06f82b42f51a1197dfc5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453352"
---
# <span data-ttu-id="c0772-101">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="c0772-101">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="c0772-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c0772-102">SYNOPSIS</span></span>
<span data-ttu-id="c0772-103">從 Linux 電腦開始收集效能計數器。</span><span class="sxs-lookup"><span data-stu-id="c0772-103">Starts collection of performance counters from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0772-104">句法</span><span class="sxs-lookup"><span data-stu-id="c0772-104">SYNTAX</span></span>

### <span data-ttu-id="c0772-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="c0772-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzureRmOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0772-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c0772-106">ByWorkspaceObject</span></span>
```
Enable-AzureRmOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0772-107">說明</span><span class="sxs-lookup"><span data-stu-id="c0772-107">DESCRIPTION</span></span>
<span data-ttu-id="c0772-108">**Enable-AzureRmOperationalInsightsLinuxPerformanceCollection** Cmdlet 會從工作區中相互連接的 Linux 電腦開始收集效能計數器。</span><span class="sxs-lookup"><span data-stu-id="c0772-108">The **Enable-AzureRmOperationalInsightsLinuxPerformanceCollection** cmdlet starts collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="c0772-109">示例</span><span class="sxs-lookup"><span data-stu-id="c0772-109">EXAMPLES</span></span>

## <span data-ttu-id="c0772-110">參數</span><span class="sxs-lookup"><span data-stu-id="c0772-110">PARAMETERS</span></span>

### <span data-ttu-id="c0772-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0772-111">-ResourceGroupName</span></span>
<span data-ttu-id="c0772-112">指定包含 Linux 電腦之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0772-112">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="c0772-113">-工作區</span><span class="sxs-lookup"><span data-stu-id="c0772-113">-Workspace</span></span>
<span data-ttu-id="c0772-114">指定這個 Cmdlet 在其中運作的工作區。</span><span class="sxs-lookup"><span data-stu-id="c0772-114">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="c0772-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c0772-115">-WorkspaceName</span></span>
<span data-ttu-id="c0772-116">指定此 Cmdlet 作用中的工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="c0772-116">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="c0772-117">-確認</span><span class="sxs-lookup"><span data-stu-id="c0772-117">-Confirm</span></span>
<span data-ttu-id="c0772-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c0772-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0772-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0772-119">-WhatIf</span></span>
<span data-ttu-id="c0772-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c0772-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0772-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c0772-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0772-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0772-122">-DefaultProfile</span></span>
<span data-ttu-id="c0772-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c0772-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0772-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0772-124">CommonParameters</span></span>
<span data-ttu-id="c0772-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c0772-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0772-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c0772-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0772-127">輸入</span><span class="sxs-lookup"><span data-stu-id="c0772-127">INPUTS</span></span>

### <span data-ttu-id="c0772-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="c0772-128">PSWorkspace</span></span>
<span data-ttu-id="c0772-129">形參 "Workspace" 接受管線中類型 ' PSWorkspace」的值</span><span class="sxs-lookup"><span data-stu-id="c0772-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="c0772-130">輸出</span><span class="sxs-lookup"><span data-stu-id="c0772-130">OUTPUTS</span></span>

### <span data-ttu-id="c0772-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="c0772-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="c0772-132">筆記</span><span class="sxs-lookup"><span data-stu-id="c0772-132">NOTES</span></span>
* <span data-ttu-id="c0772-133">關鍵字： azure，azurerm，arm，資源，管理，管理員，作業，洞察力</span><span class="sxs-lookup"><span data-stu-id="c0772-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="c0772-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0772-134">RELATED LINKS</span></span>

[<span data-ttu-id="c0772-135">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="c0772-135">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)


