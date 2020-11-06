---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/invoke-azurermdatafactoryv2integrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade.md
ms.openlocfilehash: b83e6604e854260814a949885d26968542e84efc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447395"
---
# <span data-ttu-id="16baa-101">Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="16baa-101">Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="16baa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="16baa-102">SYNOPSIS</span></span>
<span data-ttu-id="16baa-103">升級自託管的整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="16baa-103">Upgrades self-hosted integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16baa-104">句法</span><span class="sxs-lookup"><span data-stu-id="16baa-104">SYNTAX</span></span>

### <span data-ttu-id="16baa-105">ByIntegrationRuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="16baa-105">ByIntegrationRuntimeName (Default)</span></span>
```
Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16baa-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="16baa-106">ByResourceId</span></span>
```
Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16baa-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="16baa-107">ByIntegrationRuntimeObject</span></span>
```
Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16baa-108">說明</span><span class="sxs-lookup"><span data-stu-id="16baa-108">DESCRIPTION</span></span>
<span data-ttu-id="16baa-109">如果有新的版本， **AzureRmDataFactoryV2IntegrationRuntimeUpgrade** Cmdlet 會升級自託管整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="16baa-109">The **Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="16baa-110">示例</span><span class="sxs-lookup"><span data-stu-id="16baa-110">EXAMPLES</span></span>

### <span data-ttu-id="16baa-111">範例1：升級自託管整合執行時間</span><span class="sxs-lookup"><span data-stu-id="16baa-111">Example 1: Upgrades a self-hosted integration runtime</span></span>
```
PS C:\> Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="16baa-112">此 Cmdlet 會升級在資料工廠 "test-eu2" 中名為「test-selfhost-ir」的 self 託管式整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="16baa-112">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

## <span data-ttu-id="16baa-113">參數</span><span class="sxs-lookup"><span data-stu-id="16baa-113">PARAMETERS</span></span>

### <span data-ttu-id="16baa-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="16baa-114">-DataFactoryName</span></span>
<span data-ttu-id="16baa-115">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="16baa-115">The data factory name.</span></span>

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

### <span data-ttu-id="16baa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16baa-116">-DefaultProfile</span></span>
<span data-ttu-id="16baa-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="16baa-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16baa-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16baa-118">-InputObject</span></span>
<span data-ttu-id="16baa-119">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="16baa-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="16baa-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="16baa-120">-Name</span></span>
<span data-ttu-id="16baa-121">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="16baa-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="16baa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16baa-122">-ResourceGroupName</span></span>
<span data-ttu-id="16baa-123">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="16baa-123">The resource group name.</span></span>

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

### <span data-ttu-id="16baa-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16baa-124">-ResourceId</span></span>
<span data-ttu-id="16baa-125">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="16baa-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="16baa-126">-確認</span><span class="sxs-lookup"><span data-stu-id="16baa-126">-Confirm</span></span>
<span data-ttu-id="16baa-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="16baa-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16baa-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16baa-128">-WhatIf</span></span>
<span data-ttu-id="16baa-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="16baa-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16baa-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="16baa-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16baa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16baa-131">CommonParameters</span></span>
<span data-ttu-id="16baa-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="16baa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16baa-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="16baa-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16baa-134">輸入</span><span class="sxs-lookup"><span data-stu-id="16baa-134">INPUTS</span></span>

### <span data-ttu-id="16baa-135">System.object</span><span class="sxs-lookup"><span data-stu-id="16baa-135">System.String</span></span>

### <span data-ttu-id="16baa-136">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="16baa-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="16baa-137">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="16baa-137">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="16baa-138">輸出</span><span class="sxs-lookup"><span data-stu-id="16baa-138">OUTPUTS</span></span>

### <span data-ttu-id="16baa-139">System.void</span><span class="sxs-lookup"><span data-stu-id="16baa-139">System.Void</span></span>

## <span data-ttu-id="16baa-140">筆記</span><span class="sxs-lookup"><span data-stu-id="16baa-140">NOTES</span></span>
<span data-ttu-id="16baa-141">關鍵字： azure、azurerm、arm、資源、管理、管理員、資料、工廠、複本、活動、整合執行時間</span><span class="sxs-lookup"><span data-stu-id="16baa-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="16baa-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="16baa-142">RELATED LINKS</span></span>

<span data-ttu-id="16baa-143">[Set-AzureRmDataFactoryV2IntegrationRuntime]() 
[AzureRmDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="16baa-143">[Set-AzureRmDataFactoryV2IntegrationRuntime]()
[Get-AzureRmDataFactoryV2IntegrationRuntime]()</span></span>

