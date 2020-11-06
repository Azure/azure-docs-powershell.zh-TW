---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 26B1921E-6052-471B-B5B6-F2853536A425
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsIISLogCollection.md
ms.openlocfilehash: b9ab24915af941cec866fb78003d2b0e9c11267c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453356"
---
# <span data-ttu-id="26d30-101">Enable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="26d30-101">Enable-AzureRmOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="26d30-102">摘要</span><span class="sxs-lookup"><span data-stu-id="26d30-102">SYNOPSIS</span></span>
<span data-ttu-id="26d30-103">從工作區中的電腦開始收集 IIS 記錄。</span><span class="sxs-lookup"><span data-stu-id="26d30-103">Starts collection of IIS logs from computers in a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26d30-104">句法</span><span class="sxs-lookup"><span data-stu-id="26d30-104">SYNTAX</span></span>

### <span data-ttu-id="26d30-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="26d30-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzureRmOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26d30-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="26d30-106">ByWorkspaceObject</span></span>
```
Enable-AzureRmOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26d30-107">說明</span><span class="sxs-lookup"><span data-stu-id="26d30-107">DESCRIPTION</span></span>
<span data-ttu-id="26d30-108">**Enable-AzureRmOperationalInsightsIISLogCollection** Cmdlet 會開始收集網際網路資訊服務 (IIS) 記錄從工作區中的連線電腦。</span><span class="sxs-lookup"><span data-stu-id="26d30-108">The **Enable-AzureRmOperationalInsightsIISLogCollection** cmdlet starts collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="26d30-109">示例</span><span class="sxs-lookup"><span data-stu-id="26d30-109">EXAMPLES</span></span>

## <span data-ttu-id="26d30-110">參數</span><span class="sxs-lookup"><span data-stu-id="26d30-110">PARAMETERS</span></span>

### <span data-ttu-id="26d30-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26d30-111">-ResourceGroupName</span></span>
<span data-ttu-id="26d30-112">指定包含電腦之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="26d30-112">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="26d30-113">-工作區</span><span class="sxs-lookup"><span data-stu-id="26d30-113">-Workspace</span></span>
<span data-ttu-id="26d30-114">指定這個 Cmdlet 在其中運作的工作區。</span><span class="sxs-lookup"><span data-stu-id="26d30-114">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="26d30-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="26d30-115">-WorkspaceName</span></span>
<span data-ttu-id="26d30-116">指定此 Cmdlet 作用中的工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="26d30-116">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="26d30-117">-確認</span><span class="sxs-lookup"><span data-stu-id="26d30-117">-Confirm</span></span>
<span data-ttu-id="26d30-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="26d30-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26d30-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26d30-119">-WhatIf</span></span>
<span data-ttu-id="26d30-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="26d30-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26d30-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26d30-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26d30-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26d30-122">-DefaultProfile</span></span>
<span data-ttu-id="26d30-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="26d30-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26d30-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26d30-124">CommonParameters</span></span>
<span data-ttu-id="26d30-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="26d30-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26d30-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="26d30-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26d30-127">輸入</span><span class="sxs-lookup"><span data-stu-id="26d30-127">INPUTS</span></span>

### <span data-ttu-id="26d30-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="26d30-128">PSWorkspace</span></span>
<span data-ttu-id="26d30-129">形參 "Workspace" 接受管線中類型 ' PSWorkspace」的值</span><span class="sxs-lookup"><span data-stu-id="26d30-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="26d30-130">輸出</span><span class="sxs-lookup"><span data-stu-id="26d30-130">OUTPUTS</span></span>

### <span data-ttu-id="26d30-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="26d30-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="26d30-132">筆記</span><span class="sxs-lookup"><span data-stu-id="26d30-132">NOTES</span></span>

## <span data-ttu-id="26d30-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="26d30-133">RELATED LINKS</span></span>

[<span data-ttu-id="26d30-134">Disable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="26d30-134">Disable-AzureRmOperationalInsightsIISLogCollection</span></span>](./Disable-AzureRmOperationalInsightsIISLogCollection.md)


