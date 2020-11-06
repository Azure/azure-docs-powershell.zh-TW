---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: EF3FE3F1-1C8F-41EB-990E-F2B30BD9D082
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/disable-azurermoperationalinsightslinuxcustomlogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxCustomLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxCustomLogCollection.md
ms.openlocfilehash: 2eecf19ad385729bfe0a140f234f2ddf5053e746
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447327"
---
# <span data-ttu-id="e709c-101">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="e709c-101">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>

## <span data-ttu-id="e709c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e709c-102">SYNOPSIS</span></span>
<span data-ttu-id="e709c-103">停止從 Linux 電腦收集自訂記錄。</span><span class="sxs-lookup"><span data-stu-id="e709c-103">Stops collection of custom logs from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e709c-104">句法</span><span class="sxs-lookup"><span data-stu-id="e709c-104">SYNTAX</span></span>

### <span data-ttu-id="e709c-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="e709c-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzureRmOperationalInsightsLinuxCustomLogCollection [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e709c-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e709c-106">ByWorkspaceObject</span></span>
```
Disable-AzureRmOperationalInsightsLinuxCustomLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e709c-107">說明</span><span class="sxs-lookup"><span data-stu-id="e709c-107">DESCRIPTION</span></span>
<span data-ttu-id="e709c-108">**Disable AzureRmOperationalInsightsLinuxCustomLogCollection** Cmdlet 會在工作區中停止從已連接的 Linux 電腦收集自訂記錄。</span><span class="sxs-lookup"><span data-stu-id="e709c-108">The **Disable-AzureRmOperationalInsightsLinuxCustomLogCollection** cmdlet stops collection of custom logs from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="e709c-109">示例</span><span class="sxs-lookup"><span data-stu-id="e709c-109">EXAMPLES</span></span>

## <span data-ttu-id="e709c-110">參數</span><span class="sxs-lookup"><span data-stu-id="e709c-110">PARAMETERS</span></span>

### <span data-ttu-id="e709c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e709c-111">-DefaultProfile</span></span>
<span data-ttu-id="e709c-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e709c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e709c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e709c-113">-ResourceGroupName</span></span>
<span data-ttu-id="e709c-114">指定包含 Linux 電腦之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e709c-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="e709c-115">-工作區</span><span class="sxs-lookup"><span data-stu-id="e709c-115">-Workspace</span></span>
<span data-ttu-id="e709c-116">指定這個 Cmdlet 在其中運作的工作區。</span><span class="sxs-lookup"><span data-stu-id="e709c-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="e709c-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e709c-117">-WorkspaceName</span></span>
<span data-ttu-id="e709c-118">指定此 Cmdlet 作用中的工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="e709c-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="e709c-119">-確認</span><span class="sxs-lookup"><span data-stu-id="e709c-119">-Confirm</span></span>
<span data-ttu-id="e709c-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e709c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e709c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e709c-121">-WhatIf</span></span>
<span data-ttu-id="e709c-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e709c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e709c-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e709c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e709c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e709c-124">CommonParameters</span></span>
<span data-ttu-id="e709c-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e709c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e709c-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e709c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e709c-127">輸入</span><span class="sxs-lookup"><span data-stu-id="e709c-127">INPUTS</span></span>

### <span data-ttu-id="e709c-128">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="e709c-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="e709c-129">參數：工作區 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="e709c-129">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="e709c-130">System.object</span><span class="sxs-lookup"><span data-stu-id="e709c-130">System.String</span></span>

## <span data-ttu-id="e709c-131">輸出</span><span class="sxs-lookup"><span data-stu-id="e709c-131">OUTPUTS</span></span>

### <span data-ttu-id="e709c-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="e709c-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="e709c-133">筆記</span><span class="sxs-lookup"><span data-stu-id="e709c-133">NOTES</span></span>
* <span data-ttu-id="e709c-134">關鍵字： azure，azurerm，arm，資源，管理，管理員，作業，洞察力</span><span class="sxs-lookup"><span data-stu-id="e709c-134">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="e709c-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="e709c-135">RELATED LINKS</span></span>

[<span data-ttu-id="e709c-136">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="e709c-136">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)


