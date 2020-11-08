---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: E68E90B3-0B6A-49E9-83CD-E73826571B04
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightscomputergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsComputerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsComputerGroup.md
ms.openlocfilehash: 1f9afcd9e7a46110970785d9888f4b4efc4b0b70
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140634"
---
# <span data-ttu-id="9af23-101">New-AzOperationalInsightsComputerGroup</span><span class="sxs-lookup"><span data-stu-id="9af23-101">New-AzOperationalInsightsComputerGroup</span></span>

## <span data-ttu-id="9af23-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9af23-102">SYNOPSIS</span></span>
<span data-ttu-id="9af23-103">建立電腦群組。</span><span class="sxs-lookup"><span data-stu-id="9af23-103">Creates a computer group.</span></span>

## <span data-ttu-id="9af23-104">句法</span><span class="sxs-lookup"><span data-stu-id="9af23-104">SYNTAX</span></span>

```
New-AzOperationalInsightsComputerGroup [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Version] <Int64>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9af23-105">說明</span><span class="sxs-lookup"><span data-stu-id="9af23-105">DESCRIPTION</span></span>
<span data-ttu-id="9af23-106">**新的-AzOperationalInsightsComputerGroup** Cmdlet 會在資源群組和位置中建立電腦群組。</span><span class="sxs-lookup"><span data-stu-id="9af23-106">The **New-AzOperationalInsightsComputerGroup** cmdlet creates a computer group in a resource group and location.</span></span>

## <span data-ttu-id="9af23-107">示例</span><span class="sxs-lookup"><span data-stu-id="9af23-107">EXAMPLES</span></span>

### <span data-ttu-id="9af23-108">範例1</span><span class="sxs-lookup"><span data-stu-id="9af23-108">Example 1</span></span>

<span data-ttu-id="9af23-109">建立電腦群組。</span><span class="sxs-lookup"><span data-stu-id="9af23-109">Creates a computer group.</span></span> <span data-ttu-id="9af23-110"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="9af23-110">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzOperationalInsightsComputerGroup -Category 'ContosoSavedSearchCategory' -DisplayName 'ContosoSavedSearchDisplayName' -Query 'Type=Event' -ResourceGroupName myresourcegroup -SavedSearchId 'ContosoSavedSearchId' -Version 1 -WorkspaceName <String>
```

## <span data-ttu-id="9af23-111">參數</span><span class="sxs-lookup"><span data-stu-id="9af23-111">PARAMETERS</span></span>

### <span data-ttu-id="9af23-112">-類別</span><span class="sxs-lookup"><span data-stu-id="9af23-112">-Category</span></span>
<span data-ttu-id="9af23-113">指定電腦群組的類別。</span><span class="sxs-lookup"><span data-stu-id="9af23-113">Specifies the category of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9af23-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9af23-114">-DefaultProfile</span></span>
<span data-ttu-id="9af23-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="9af23-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9af23-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9af23-116">-DisplayName</span></span>
<span data-ttu-id="9af23-117">指定電腦群組的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="9af23-117">Specifies the display name of the computer group.</span></span>

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

### <span data-ttu-id="9af23-118">-Force</span><span class="sxs-lookup"><span data-stu-id="9af23-118">-Force</span></span>
<span data-ttu-id="9af23-119">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="9af23-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9af23-120">-Query</span><span class="sxs-lookup"><span data-stu-id="9af23-120">-Query</span></span>
<span data-ttu-id="9af23-121">指定電腦群組的查詢。</span><span class="sxs-lookup"><span data-stu-id="9af23-121">Specifies the query of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9af23-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9af23-122">-ResourceGroupName</span></span>
<span data-ttu-id="9af23-123">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9af23-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="9af23-124">此 Cmdlet 會在此資源群組中建立電腦群組。</span><span class="sxs-lookup"><span data-stu-id="9af23-124">The cmdlet creates computer group in this resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9af23-125">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="9af23-125">-SavedSearchId</span></span>
<span data-ttu-id="9af23-126">指定電腦群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9af23-126">Specifies the ID of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9af23-127">-版本</span><span class="sxs-lookup"><span data-stu-id="9af23-127">-Version</span></span>
<span data-ttu-id="9af23-128">指定版本。</span><span class="sxs-lookup"><span data-stu-id="9af23-128">Specifies the version.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: 1
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9af23-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9af23-129">-WorkspaceName</span></span>
<span data-ttu-id="9af23-130">指定工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="9af23-130">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9af23-131">-確認</span><span class="sxs-lookup"><span data-stu-id="9af23-131">-Confirm</span></span>
<span data-ttu-id="9af23-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9af23-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9af23-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9af23-133">-WhatIf</span></span>
<span data-ttu-id="9af23-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9af23-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9af23-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9af23-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9af23-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9af23-136">CommonParameters</span></span>
<span data-ttu-id="9af23-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9af23-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9af23-138">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9af23-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9af23-139">輸入</span><span class="sxs-lookup"><span data-stu-id="9af23-139">INPUTS</span></span>

### <span data-ttu-id="9af23-140">System.object</span><span class="sxs-lookup"><span data-stu-id="9af23-140">System.String</span></span>

### <span data-ttu-id="9af23-141">System.object</span><span class="sxs-lookup"><span data-stu-id="9af23-141">System.Int64</span></span>

## <span data-ttu-id="9af23-142">輸出</span><span class="sxs-lookup"><span data-stu-id="9af23-142">OUTPUTS</span></span>

### <span data-ttu-id="9af23-143">HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="9af23-143">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="9af23-144">筆記</span><span class="sxs-lookup"><span data-stu-id="9af23-144">NOTES</span></span>

## <span data-ttu-id="9af23-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="9af23-145">RELATED LINKS</span></span>