---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: E68E90B3-0B6A-49E9-83CD-E73826571B04
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsComputerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsComputerGroup.md
ms.openlocfilehash: 8a54a735b41ef537a31f5e3e1ce2789d10e60af6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449578"
---
# <span data-ttu-id="bcb90-101">New-AzureRmOperationalInsightsComputerGroup</span><span class="sxs-lookup"><span data-stu-id="bcb90-101">New-AzureRmOperationalInsightsComputerGroup</span></span>

## <span data-ttu-id="bcb90-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bcb90-102">SYNOPSIS</span></span>
<span data-ttu-id="bcb90-103">建立電腦群組。</span><span class="sxs-lookup"><span data-stu-id="bcb90-103">Creates a computer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcb90-104">句法</span><span class="sxs-lookup"><span data-stu-id="bcb90-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsComputerGroup [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Version] <Int64>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcb90-105">說明</span><span class="sxs-lookup"><span data-stu-id="bcb90-105">DESCRIPTION</span></span>
<span data-ttu-id="bcb90-106">**新的-AzureRmOperationalInsightsComputerGroup** Cmdlet 會在資源群組和位置中建立電腦群組。</span><span class="sxs-lookup"><span data-stu-id="bcb90-106">The **New-AzureRmOperationalInsightsComputerGroup** cmdlet creates a computer group in a resource group and location.</span></span>

## <span data-ttu-id="bcb90-107">示例</span><span class="sxs-lookup"><span data-stu-id="bcb90-107">EXAMPLES</span></span>

## <span data-ttu-id="bcb90-108">參數</span><span class="sxs-lookup"><span data-stu-id="bcb90-108">PARAMETERS</span></span>

### <span data-ttu-id="bcb90-109">-類別</span><span class="sxs-lookup"><span data-stu-id="bcb90-109">-Category</span></span>
<span data-ttu-id="bcb90-110">指定電腦群組的類別。</span><span class="sxs-lookup"><span data-stu-id="bcb90-110">Specifies the category of the computer group.</span></span>

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

### <span data-ttu-id="bcb90-111">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="bcb90-111">-DisplayName</span></span>
<span data-ttu-id="bcb90-112">指定電腦群組的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="bcb90-112">Specifies the display name of the computer group.</span></span>

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

### <span data-ttu-id="bcb90-113">-Force</span><span class="sxs-lookup"><span data-stu-id="bcb90-113">-Force</span></span>
<span data-ttu-id="bcb90-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="bcb90-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bcb90-115">-Query</span><span class="sxs-lookup"><span data-stu-id="bcb90-115">-Query</span></span>
<span data-ttu-id="bcb90-116">指定電腦群組的查詢。</span><span class="sxs-lookup"><span data-stu-id="bcb90-116">Specifies the query of the computer group.</span></span>

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

### <span data-ttu-id="bcb90-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcb90-117">-ResourceGroupName</span></span>
<span data-ttu-id="bcb90-118">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bcb90-118">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="bcb90-119">此 Cmdlet 會在此資源群組中建立電腦群組。</span><span class="sxs-lookup"><span data-stu-id="bcb90-119">The cmdlet creates computer group in this resource group.</span></span>

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

### <span data-ttu-id="bcb90-120">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="bcb90-120">-SavedSearchId</span></span>
<span data-ttu-id="bcb90-121">指定電腦群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="bcb90-121">Specifies the ID of the computer group.</span></span>

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

### <span data-ttu-id="bcb90-122">-版本</span><span class="sxs-lookup"><span data-stu-id="bcb90-122">-Version</span></span>
<span data-ttu-id="bcb90-123">指定版本。</span><span class="sxs-lookup"><span data-stu-id="bcb90-123">Specifies the version.</span></span>

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

### <span data-ttu-id="bcb90-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bcb90-124">-WorkspaceName</span></span>
<span data-ttu-id="bcb90-125">指定工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="bcb90-125">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="bcb90-126">-確認</span><span class="sxs-lookup"><span data-stu-id="bcb90-126">-Confirm</span></span>
<span data-ttu-id="bcb90-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bcb90-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcb90-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcb90-128">-WhatIf</span></span>
<span data-ttu-id="bcb90-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bcb90-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcb90-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bcb90-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcb90-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcb90-131">-DefaultProfile</span></span>
<span data-ttu-id="bcb90-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bcb90-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcb90-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcb90-133">CommonParameters</span></span>
<span data-ttu-id="bcb90-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bcb90-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcb90-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bcb90-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcb90-136">輸入</span><span class="sxs-lookup"><span data-stu-id="bcb90-136">INPUTS</span></span>

## <span data-ttu-id="bcb90-137">輸出</span><span class="sxs-lookup"><span data-stu-id="bcb90-137">OUTPUTS</span></span>

## <span data-ttu-id="bcb90-138">筆記</span><span class="sxs-lookup"><span data-stu-id="bcb90-138">NOTES</span></span>

## <span data-ttu-id="bcb90-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="bcb90-139">RELATED LINKS</span></span>

