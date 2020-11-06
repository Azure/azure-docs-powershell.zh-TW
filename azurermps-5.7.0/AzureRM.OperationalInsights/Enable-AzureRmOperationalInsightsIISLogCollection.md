---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 26B1921E-6052-471B-B5B6-F2853536A425
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/enable-azurermoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsIISLogCollection.md
ms.openlocfilehash: 417bc080d707c3da02dd8a0083fb707f79d0a999
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449256"
---
# <span data-ttu-id="261bf-101">Enable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="261bf-101">Enable-AzureRmOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="261bf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="261bf-102">SYNOPSIS</span></span>
<span data-ttu-id="261bf-103">從工作區中的電腦開始收集 IIS 記錄。</span><span class="sxs-lookup"><span data-stu-id="261bf-103">Starts collection of IIS logs from computers in a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="261bf-104">句法</span><span class="sxs-lookup"><span data-stu-id="261bf-104">SYNTAX</span></span>

### <span data-ttu-id="261bf-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="261bf-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzureRmOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="261bf-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="261bf-106">ByWorkspaceObject</span></span>
```
Enable-AzureRmOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="261bf-107">說明</span><span class="sxs-lookup"><span data-stu-id="261bf-107">DESCRIPTION</span></span>
<span data-ttu-id="261bf-108">**Enable-AzureRmOperationalInsightsIISLogCollection** Cmdlet 會開始收集網際網路資訊服務 (IIS) 記錄從工作區中的連線電腦。</span><span class="sxs-lookup"><span data-stu-id="261bf-108">The **Enable-AzureRmOperationalInsightsIISLogCollection** cmdlet starts collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="261bf-109">示例</span><span class="sxs-lookup"><span data-stu-id="261bf-109">EXAMPLES</span></span>

## <span data-ttu-id="261bf-110">參數</span><span class="sxs-lookup"><span data-stu-id="261bf-110">PARAMETERS</span></span>

### <span data-ttu-id="261bf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="261bf-111">-DefaultProfile</span></span>
<span data-ttu-id="261bf-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="261bf-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="261bf-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="261bf-113">-ResourceGroupName</span></span>
<span data-ttu-id="261bf-114">指定包含電腦之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="261bf-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="261bf-115">-工作區</span><span class="sxs-lookup"><span data-stu-id="261bf-115">-Workspace</span></span>
<span data-ttu-id="261bf-116">指定這個 Cmdlet 在其中運作的工作區。</span><span class="sxs-lookup"><span data-stu-id="261bf-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="261bf-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="261bf-117">-WorkspaceName</span></span>
<span data-ttu-id="261bf-118">指定此 Cmdlet 作用中的工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="261bf-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="261bf-119">-確認</span><span class="sxs-lookup"><span data-stu-id="261bf-119">-Confirm</span></span>
<span data-ttu-id="261bf-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="261bf-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="261bf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="261bf-121">-WhatIf</span></span>
<span data-ttu-id="261bf-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="261bf-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="261bf-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="261bf-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="261bf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="261bf-124">CommonParameters</span></span>
<span data-ttu-id="261bf-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="261bf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="261bf-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="261bf-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="261bf-127">輸入</span><span class="sxs-lookup"><span data-stu-id="261bf-127">INPUTS</span></span>

### <span data-ttu-id="261bf-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="261bf-128">PSWorkspace</span></span>
<span data-ttu-id="261bf-129">形參 "Workspace" 接受管線中類型 ' PSWorkspace」的值</span><span class="sxs-lookup"><span data-stu-id="261bf-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="261bf-130">輸出</span><span class="sxs-lookup"><span data-stu-id="261bf-130">OUTPUTS</span></span>

### <span data-ttu-id="261bf-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="261bf-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="261bf-132">筆記</span><span class="sxs-lookup"><span data-stu-id="261bf-132">NOTES</span></span>

## <span data-ttu-id="261bf-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="261bf-133">RELATED LINKS</span></span>

[<span data-ttu-id="261bf-134">Disable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="261bf-134">Disable-AzureRmOperationalInsightsIISLogCollection</span></span>](./Disable-AzureRmOperationalInsightsIISLogCollection.md)


