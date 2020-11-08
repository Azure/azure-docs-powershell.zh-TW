---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2integrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade.md
ms.openlocfilehash: c7ffe4348d11658da6e7c9caeccaa14f17a6329b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128274"
---
# <span data-ttu-id="fa2a2-101">Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="fa2a2-101">Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="fa2a2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fa2a2-102">SYNOPSIS</span></span>
<span data-ttu-id="fa2a2-103">升級自託管的整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="fa2a2-103">Upgrades self-hosted integration runtime.</span></span>

## <span data-ttu-id="fa2a2-104">句法</span><span class="sxs-lookup"><span data-stu-id="fa2a2-104">SYNTAX</span></span>

### <span data-ttu-id="fa2a2-105">ByIntegrationRuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="fa2a2-105">ByIntegrationRuntimeName (Default)</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fa2a2-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fa2a2-106">ByResourceId</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa2a2-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="fa2a2-107">ByIntegrationRuntimeObject</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa2a2-108">說明</span><span class="sxs-lookup"><span data-stu-id="fa2a2-108">DESCRIPTION</span></span>
<span data-ttu-id="fa2a2-109">如果有新的版本， **AzDataFactoryV2IntegrationRuntimeUpgrade** Cmdlet 會升級自託管整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="fa2a2-109">The **Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="fa2a2-110">示例</span><span class="sxs-lookup"><span data-stu-id="fa2a2-110">EXAMPLES</span></span>

### <span data-ttu-id="fa2a2-111">範例1：升級自託管整合執行時間</span><span class="sxs-lookup"><span data-stu-id="fa2a2-111">Example 1: Upgrades a self-hosted integration runtime</span></span>
```
PS C:\> Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="fa2a2-112">此 Cmdlet 會升級在資料工廠 "test-eu2" 中名為「test-selfhost-ir」的 self 託管式整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="fa2a2-112">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

## <span data-ttu-id="fa2a2-113">參數</span><span class="sxs-lookup"><span data-stu-id="fa2a2-113">PARAMETERS</span></span>

### <span data-ttu-id="fa2a2-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="fa2a2-114">-DataFactoryName</span></span>
<span data-ttu-id="fa2a2-115">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="fa2a2-115">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa2a2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa2a2-116">-DefaultProfile</span></span>
<span data-ttu-id="fa2a2-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fa2a2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa2a2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa2a2-118">-InputObject</span></span>
<span data-ttu-id="fa2a2-119">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="fa2a2-119">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa2a2-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="fa2a2-120">-Name</span></span>
<span data-ttu-id="fa2a2-121">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="fa2a2-121">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa2a2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa2a2-122">-ResourceGroupName</span></span>
<span data-ttu-id="fa2a2-123">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fa2a2-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa2a2-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa2a2-124">-ResourceId</span></span>
<span data-ttu-id="fa2a2-125">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="fa2a2-125">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa2a2-126">-確認</span><span class="sxs-lookup"><span data-stu-id="fa2a2-126">-Confirm</span></span>
<span data-ttu-id="fa2a2-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fa2a2-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa2a2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa2a2-128">-WhatIf</span></span>
<span data-ttu-id="fa2a2-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fa2a2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa2a2-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fa2a2-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa2a2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa2a2-131">CommonParameters</span></span>
<span data-ttu-id="fa2a2-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fa2a2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa2a2-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fa2a2-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa2a2-134">輸入</span><span class="sxs-lookup"><span data-stu-id="fa2a2-134">INPUTS</span></span>

### <span data-ttu-id="fa2a2-135">System.object</span><span class="sxs-lookup"><span data-stu-id="fa2a2-135">System.String</span></span>

### <span data-ttu-id="fa2a2-136">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="fa2a2-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="fa2a2-137">輸出</span><span class="sxs-lookup"><span data-stu-id="fa2a2-137">OUTPUTS</span></span>

### <span data-ttu-id="fa2a2-138">System.void</span><span class="sxs-lookup"><span data-stu-id="fa2a2-138">System.Void</span></span>

## <span data-ttu-id="fa2a2-139">筆記</span><span class="sxs-lookup"><span data-stu-id="fa2a2-139">NOTES</span></span>
<span data-ttu-id="fa2a2-140">關鍵字： azure、azurerm、arm、資源、管理、管理員、資料、工廠、複本、活動、整合執行時間</span><span class="sxs-lookup"><span data-stu-id="fa2a2-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="fa2a2-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="fa2a2-141">RELATED LINKS</span></span>

<span data-ttu-id="fa2a2-142">[Set-AzDataFactoryV2IntegrationRuntime]() 
[AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="fa2a2-142">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>
