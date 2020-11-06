---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 5C1C51FE-747F-4176-84ED-A28AA3475581
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: e9d5a7443c8a758cdc839826025d51fe57d55420
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450186"
---
# <span data-ttu-id="6175e-101">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="6175e-101">Remove-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="6175e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6175e-102">SYNOPSIS</span></span>
<span data-ttu-id="6175e-103">刪除資料來源。</span><span class="sxs-lookup"><span data-stu-id="6175e-103">Deletes a data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6175e-104">句法</span><span class="sxs-lookup"><span data-stu-id="6175e-104">SYNTAX</span></span>

### <span data-ttu-id="6175e-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="6175e-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzureRmOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6175e-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6175e-106">ByWorkspaceObject</span></span>
```
Remove-AzureRmOperationalInsightsDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6175e-107">說明</span><span class="sxs-lookup"><span data-stu-id="6175e-107">DESCRIPTION</span></span>
<span data-ttu-id="6175e-108">**AzureRmOperationalInsightsDataSource** Cmdlet 會刪除資料來源。</span><span class="sxs-lookup"><span data-stu-id="6175e-108">The **Remove-AzureRmOperationalInsightsDataSource** cmdlet deletes a data source.</span></span>

## <span data-ttu-id="6175e-109">示例</span><span class="sxs-lookup"><span data-stu-id="6175e-109">EXAMPLES</span></span>

## <span data-ttu-id="6175e-110">參數</span><span class="sxs-lookup"><span data-stu-id="6175e-110">PARAMETERS</span></span>

### <span data-ttu-id="6175e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6175e-111">-DefaultProfile</span></span>
<span data-ttu-id="6175e-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="6175e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6175e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="6175e-113">-Force</span></span>
<span data-ttu-id="6175e-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="6175e-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6175e-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="6175e-115">-Name</span></span>
<span data-ttu-id="6175e-116">指定要刪除的資料來源名稱。</span><span class="sxs-lookup"><span data-stu-id="6175e-116">Specifies the name of a data source to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6175e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6175e-117">-ResourceGroupName</span></span>
<span data-ttu-id="6175e-118">指定包含電腦之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6175e-118">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="6175e-119">-工作區</span><span class="sxs-lookup"><span data-stu-id="6175e-119">-Workspace</span></span>
<span data-ttu-id="6175e-120">指定這個 Cmdlet 在其中運作的工作區。</span><span class="sxs-lookup"><span data-stu-id="6175e-120">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="6175e-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6175e-121">-WorkspaceName</span></span>
<span data-ttu-id="6175e-122">指定此 Cmdlet 作用中的工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="6175e-122">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="6175e-123">-確認</span><span class="sxs-lookup"><span data-stu-id="6175e-123">-Confirm</span></span>
<span data-ttu-id="6175e-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6175e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6175e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6175e-125">-WhatIf</span></span>
<span data-ttu-id="6175e-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6175e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6175e-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6175e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6175e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6175e-128">CommonParameters</span></span>
<span data-ttu-id="6175e-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6175e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6175e-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6175e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6175e-131">輸入</span><span class="sxs-lookup"><span data-stu-id="6175e-131">INPUTS</span></span>

### <span data-ttu-id="6175e-132">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="6175e-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="6175e-133">參數：工作區 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="6175e-133">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="6175e-134">System.object</span><span class="sxs-lookup"><span data-stu-id="6175e-134">System.String</span></span>

## <span data-ttu-id="6175e-135">輸出</span><span class="sxs-lookup"><span data-stu-id="6175e-135">OUTPUTS</span></span>

### <span data-ttu-id="6175e-136">System.void</span><span class="sxs-lookup"><span data-stu-id="6175e-136">System.Void</span></span>

## <span data-ttu-id="6175e-137">筆記</span><span class="sxs-lookup"><span data-stu-id="6175e-137">NOTES</span></span>
* <span data-ttu-id="6175e-138">關鍵字： azure，azurerm，arm，資源，管理，管理員，作業，洞察力</span><span class="sxs-lookup"><span data-stu-id="6175e-138">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="6175e-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="6175e-139">RELATED LINKS</span></span>

[<span data-ttu-id="6175e-140">AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="6175e-140">Get-AzureRmOperationalInsightsDataSource</span></span>](./Get-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="6175e-141">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="6175e-141">Set-AzureRmOperationalInsightsDataSource</span></span>](./Set-AzureRmOperationalInsightsDataSource.md)


