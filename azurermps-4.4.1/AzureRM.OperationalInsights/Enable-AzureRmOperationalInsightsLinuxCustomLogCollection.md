---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 99865242-6623-425E-92F2-0B229FC4EDAC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxCustomLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxCustomLogCollection.md
ms.openlocfilehash: 0b907f07280eae32ecb208fd13195767145c9541
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453355"
---
# <span data-ttu-id="54c63-101">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="54c63-101">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>

## <span data-ttu-id="54c63-102">摘要</span><span class="sxs-lookup"><span data-stu-id="54c63-102">SYNOPSIS</span></span>
<span data-ttu-id="54c63-103">從 Linux 電腦開始收集自訂記錄。</span><span class="sxs-lookup"><span data-stu-id="54c63-103">Starts collection of custom logs from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54c63-104">句法</span><span class="sxs-lookup"><span data-stu-id="54c63-104">SYNTAX</span></span>

### <span data-ttu-id="54c63-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="54c63-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzureRmOperationalInsightsLinuxCustomLogCollection [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54c63-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="54c63-106">ByWorkspaceObject</span></span>
```
Enable-AzureRmOperationalInsightsLinuxCustomLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54c63-107">說明</span><span class="sxs-lookup"><span data-stu-id="54c63-107">DESCRIPTION</span></span>
<span data-ttu-id="54c63-108">**Enable-AzureRmOperationalInsightsLinuxCustomLogCollection** Cmdlet 會從工作區中相互連接的 Linux 電腦開始收集自訂記錄。</span><span class="sxs-lookup"><span data-stu-id="54c63-108">The **Enable-AzureRmOperationalInsightsLinuxCustomLogCollection** cmdlet starts collection of custom logs from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="54c63-109">示例</span><span class="sxs-lookup"><span data-stu-id="54c63-109">EXAMPLES</span></span>

## <span data-ttu-id="54c63-110">參數</span><span class="sxs-lookup"><span data-stu-id="54c63-110">PARAMETERS</span></span>

### <span data-ttu-id="54c63-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54c63-111">-ResourceGroupName</span></span>
<span data-ttu-id="54c63-112">指定包含 Linux 電腦之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="54c63-112">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="54c63-113">-工作區</span><span class="sxs-lookup"><span data-stu-id="54c63-113">-Workspace</span></span>
<span data-ttu-id="54c63-114">指定這個 Cmdlet 在其中運作的工作區。</span><span class="sxs-lookup"><span data-stu-id="54c63-114">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="54c63-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="54c63-115">-WorkspaceName</span></span>
<span data-ttu-id="54c63-116">指定此 Cmdlet 作用中的工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="54c63-116">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="54c63-117">-確認</span><span class="sxs-lookup"><span data-stu-id="54c63-117">-Confirm</span></span>
<span data-ttu-id="54c63-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="54c63-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54c63-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54c63-119">-WhatIf</span></span>
<span data-ttu-id="54c63-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="54c63-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54c63-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="54c63-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54c63-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54c63-122">-DefaultProfile</span></span>
<span data-ttu-id="54c63-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="54c63-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54c63-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54c63-124">CommonParameters</span></span>
<span data-ttu-id="54c63-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="54c63-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54c63-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="54c63-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54c63-127">輸入</span><span class="sxs-lookup"><span data-stu-id="54c63-127">INPUTS</span></span>

### <span data-ttu-id="54c63-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="54c63-128">PSWorkspace</span></span>
<span data-ttu-id="54c63-129">形參 "Workspace" 接受管線中類型 ' PSWorkspace」的值</span><span class="sxs-lookup"><span data-stu-id="54c63-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="54c63-130">輸出</span><span class="sxs-lookup"><span data-stu-id="54c63-130">OUTPUTS</span></span>

### <span data-ttu-id="54c63-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="54c63-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="54c63-132">筆記</span><span class="sxs-lookup"><span data-stu-id="54c63-132">NOTES</span></span>
* <span data-ttu-id="54c63-133">關鍵字： azure，azurerm，arm，資源，管理，管理員，作業，洞察力</span><span class="sxs-lookup"><span data-stu-id="54c63-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="54c63-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="54c63-134">RELATED LINKS</span></span>

[<span data-ttu-id="54c63-135">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="54c63-135">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)


