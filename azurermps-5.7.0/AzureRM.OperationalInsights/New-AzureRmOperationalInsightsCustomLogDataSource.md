---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 6A08AF7C-1E18-40A1-B21E-12F94823D304
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightscustomlogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsCustomLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsCustomLogDataSource.md
ms.openlocfilehash: 510148c5d700c1378b0e468bbd5e8a9206491284
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457067"
---
# <span data-ttu-id="fa762-101">New-AzureRmOperationalInsightsCustomLogDataSource</span><span class="sxs-lookup"><span data-stu-id="fa762-101">New-AzureRmOperationalInsightsCustomLogDataSource</span></span>

## <span data-ttu-id="fa762-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fa762-102">SYNOPSIS</span></span>
<span data-ttu-id="fa762-103">定義自訂的日誌收集原則。</span><span class="sxs-lookup"><span data-stu-id="fa762-103">Defines a custom log collection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa762-104">句法</span><span class="sxs-lookup"><span data-stu-id="fa762-104">SYNTAX</span></span>

### <span data-ttu-id="fa762-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="fa762-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsCustomLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa762-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="fa762-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsCustomLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fa762-107">說明</span><span class="sxs-lookup"><span data-stu-id="fa762-107">DESCRIPTION</span></span>
<span data-ttu-id="fa762-108">**新的-AzureRmOperationalInsightsCustomLogDataSource** Cmdlet 定義自訂的記錄集合原則。</span><span class="sxs-lookup"><span data-stu-id="fa762-108">The **New-AzureRmOperationalInsightsCustomLogDataSource** cmdlet defines a custom log collection policy.</span></span>

## <span data-ttu-id="fa762-109">示例</span><span class="sxs-lookup"><span data-stu-id="fa762-109">EXAMPLES</span></span>

## <span data-ttu-id="fa762-110">參數</span><span class="sxs-lookup"><span data-stu-id="fa762-110">PARAMETERS</span></span>

### <span data-ttu-id="fa762-111">-CustomLogRawJson</span><span class="sxs-lookup"><span data-stu-id="fa762-111">-CustomLogRawJson</span></span>
<span data-ttu-id="fa762-112">將自訂集合原則指定為原始 JavaScript 物件符號 (JSON) 字串。</span><span class="sxs-lookup"><span data-stu-id="fa762-112">Specifies the custom collection policy as a raw JavaScript Object Notation (JSON) string.</span></span>

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

### <span data-ttu-id="fa762-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa762-113">-DefaultProfile</span></span>
<span data-ttu-id="fa762-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="fa762-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa762-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fa762-115">-Force</span></span>
<span data-ttu-id="fa762-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="fa762-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fa762-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="fa762-117">-Name</span></span>
<span data-ttu-id="fa762-118">指定資料來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="fa762-118">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="fa762-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa762-119">-ResourceGroupName</span></span>
<span data-ttu-id="fa762-120">指定包含電腦之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fa762-120">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="fa762-121">-工作區</span><span class="sxs-lookup"><span data-stu-id="fa762-121">-Workspace</span></span>
<span data-ttu-id="fa762-122">指定這個 Cmdlet 在其中運作的工作區。</span><span class="sxs-lookup"><span data-stu-id="fa762-122">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="fa762-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fa762-123">-WorkspaceName</span></span>
<span data-ttu-id="fa762-124">指定此 Cmdlet 作用中的工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="fa762-124">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="fa762-125">-確認</span><span class="sxs-lookup"><span data-stu-id="fa762-125">-Confirm</span></span>
<span data-ttu-id="fa762-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fa762-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa762-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa762-127">-WhatIf</span></span>
<span data-ttu-id="fa762-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fa762-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa762-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fa762-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa762-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa762-130">CommonParameters</span></span>
<span data-ttu-id="fa762-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fa762-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa762-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fa762-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa762-133">輸入</span><span class="sxs-lookup"><span data-stu-id="fa762-133">INPUTS</span></span>

### <span data-ttu-id="fa762-134">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="fa762-134">PSWorkspace</span></span>
<span data-ttu-id="fa762-135">形參 "Workspace" 接受管線中類型 ' PSWorkspace」的值</span><span class="sxs-lookup"><span data-stu-id="fa762-135">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="fa762-136">輸出</span><span class="sxs-lookup"><span data-stu-id="fa762-136">OUTPUTS</span></span>

### <span data-ttu-id="fa762-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="fa762-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="fa762-138">筆記</span><span class="sxs-lookup"><span data-stu-id="fa762-138">NOTES</span></span>

## <span data-ttu-id="fa762-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="fa762-139">RELATED LINKS</span></span>

[<span data-ttu-id="fa762-140">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="fa762-140">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)

[<span data-ttu-id="fa762-141">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="fa762-141">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)


