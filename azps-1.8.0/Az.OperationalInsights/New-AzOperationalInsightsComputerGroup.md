---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: E68E90B3-0B6A-49E9-83CD-E73826571B04
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightscomputergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsComputerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsComputerGroup.md
ms.openlocfilehash: ce3a935dc97e63615e3bb1253fd5eedcb5c702da
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621294"
---
# <span data-ttu-id="ba8ed-101">New-AzOperationalInsightsComputerGroup</span><span class="sxs-lookup"><span data-stu-id="ba8ed-101">New-AzOperationalInsightsComputerGroup</span></span>

## <span data-ttu-id="ba8ed-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ba8ed-102">SYNOPSIS</span></span>
<span data-ttu-id="ba8ed-103">建立電腦群組。</span><span class="sxs-lookup"><span data-stu-id="ba8ed-103">Creates a computer group.</span></span>

## <span data-ttu-id="ba8ed-104">句法</span><span class="sxs-lookup"><span data-stu-id="ba8ed-104">SYNTAX</span></span>

```
New-AzOperationalInsightsComputerGroup [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Version] <Int64>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba8ed-105">說明</span><span class="sxs-lookup"><span data-stu-id="ba8ed-105">DESCRIPTION</span></span>
<span data-ttu-id="ba8ed-106">**新的-AzOperationalInsightsComputerGroup** Cmdlet 會在資源群組和位置中建立電腦群組。</span><span class="sxs-lookup"><span data-stu-id="ba8ed-106">The **New-AzOperationalInsightsComputerGroup** cmdlet creates a computer group in a resource group and location.</span></span>

## <span data-ttu-id="ba8ed-107">示例</span><span class="sxs-lookup"><span data-stu-id="ba8ed-107">EXAMPLES</span></span>

## <span data-ttu-id="ba8ed-108">參數</span><span class="sxs-lookup"><span data-stu-id="ba8ed-108">PARAMETERS</span></span>

### <span data-ttu-id="ba8ed-109">-類別</span><span class="sxs-lookup"><span data-stu-id="ba8ed-109">-Category</span></span>
<span data-ttu-id="ba8ed-110">指定電腦群組的類別。</span><span class="sxs-lookup"><span data-stu-id="ba8ed-110">Specifies the category of the computer group.</span></span>

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

### <span data-ttu-id="ba8ed-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba8ed-111">-DefaultProfile</span></span>
<span data-ttu-id="ba8ed-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ba8ed-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba8ed-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ba8ed-113">-DisplayName</span></span>
<span data-ttu-id="ba8ed-114">指定電腦群組的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="ba8ed-114">Specifies the display name of the computer group.</span></span>

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

### <span data-ttu-id="ba8ed-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ba8ed-115">-Force</span></span>
<span data-ttu-id="ba8ed-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="ba8ed-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ba8ed-117">-Query</span><span class="sxs-lookup"><span data-stu-id="ba8ed-117">-Query</span></span>
<span data-ttu-id="ba8ed-118">指定電腦群組的查詢。</span><span class="sxs-lookup"><span data-stu-id="ba8ed-118">Specifies the query of the computer group.</span></span>

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

### <span data-ttu-id="ba8ed-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba8ed-119">-ResourceGroupName</span></span>
<span data-ttu-id="ba8ed-120">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba8ed-120">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ba8ed-121">此 Cmdlet 會在此資源群組中建立電腦群組。</span><span class="sxs-lookup"><span data-stu-id="ba8ed-121">The cmdlet creates computer group in this resource group.</span></span>

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

### <span data-ttu-id="ba8ed-122">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="ba8ed-122">-SavedSearchId</span></span>
<span data-ttu-id="ba8ed-123">指定電腦群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ba8ed-123">Specifies the ID of the computer group.</span></span>

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

### <span data-ttu-id="ba8ed-124">-版本</span><span class="sxs-lookup"><span data-stu-id="ba8ed-124">-Version</span></span>
<span data-ttu-id="ba8ed-125">指定版本。</span><span class="sxs-lookup"><span data-stu-id="ba8ed-125">Specifies the version.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba8ed-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ba8ed-126">-WorkspaceName</span></span>
<span data-ttu-id="ba8ed-127">指定工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba8ed-127">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="ba8ed-128">-確認</span><span class="sxs-lookup"><span data-stu-id="ba8ed-128">-Confirm</span></span>
<span data-ttu-id="ba8ed-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ba8ed-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba8ed-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba8ed-130">-WhatIf</span></span>
<span data-ttu-id="ba8ed-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ba8ed-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba8ed-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ba8ed-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba8ed-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba8ed-133">CommonParameters</span></span>
<span data-ttu-id="ba8ed-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ba8ed-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba8ed-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ba8ed-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba8ed-136">輸入</span><span class="sxs-lookup"><span data-stu-id="ba8ed-136">INPUTS</span></span>

### <span data-ttu-id="ba8ed-137">System.object</span><span class="sxs-lookup"><span data-stu-id="ba8ed-137">System.String</span></span>

### <span data-ttu-id="ba8ed-138">System.object</span><span class="sxs-lookup"><span data-stu-id="ba8ed-138">System.Int64</span></span>

## <span data-ttu-id="ba8ed-139">輸出</span><span class="sxs-lookup"><span data-stu-id="ba8ed-139">OUTPUTS</span></span>

### <span data-ttu-id="ba8ed-140">HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="ba8ed-140">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="ba8ed-141">筆記</span><span class="sxs-lookup"><span data-stu-id="ba8ed-141">NOTES</span></span>

## <span data-ttu-id="ba8ed-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="ba8ed-142">RELATED LINKS</span></span>
