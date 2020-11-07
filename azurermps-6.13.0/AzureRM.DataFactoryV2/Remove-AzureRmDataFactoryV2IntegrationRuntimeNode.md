---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: 413125f6bcc9935ffae66551ba5bd178eb4a3c53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623420"
---
# <span data-ttu-id="ae171-101">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="ae171-101">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="ae171-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ae171-102">SYNOPSIS</span></span>
<span data-ttu-id="ae171-103">在整合執行時間中移除具有指定名稱的節點。</span><span class="sxs-lookup"><span data-stu-id="ae171-103">Remove a node with the given name on an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae171-104">句法</span><span class="sxs-lookup"><span data-stu-id="ae171-104">SYNTAX</span></span>

### <span data-ttu-id="ae171-105">ByIntegrationRuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="ae171-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force]
 [-IntegrationRuntimeName] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae171-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ae171-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae171-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="ae171-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ae171-108">說明</span><span class="sxs-lookup"><span data-stu-id="ae171-108">DESCRIPTION</span></span>
<span data-ttu-id="ae171-109">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode Cmdlet 會移除整合執行時間中的節點。</span><span class="sxs-lookup"><span data-stu-id="ae171-109">The Remove-AzureRmDataFactoryV2IntegrationRuntimeNode cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="ae171-110">示例</span><span class="sxs-lookup"><span data-stu-id="ae171-110">EXAMPLES</span></span>

### <span data-ttu-id="ae171-111">範例1：從整合執行時間中移除節點</span><span class="sxs-lookup"><span data-stu-id="ae171-111">Example 1: Remove a node from an integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="ae171-112">這個命令會移除名為「rg-test-dfv2」的整合執行時間中名為「Node_1」的節點，以及名為「test-eu2」的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="ae171-112">This command removes an node named 'Node_1' in the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="ae171-113">參數</span><span class="sxs-lookup"><span data-stu-id="ae171-113">PARAMETERS</span></span>

### <span data-ttu-id="ae171-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ae171-114">-DataFactoryName</span></span>
<span data-ttu-id="ae171-115">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="ae171-115">The data factory name.</span></span>

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

### <span data-ttu-id="ae171-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae171-116">-DefaultProfile</span></span>
<span data-ttu-id="ae171-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ae171-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae171-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ae171-118">-Force</span></span>
<span data-ttu-id="ae171-119">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ae171-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ae171-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae171-120">-InputObject</span></span>
<span data-ttu-id="ae171-121">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="ae171-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="ae171-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="ae171-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="ae171-123">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="ae171-123">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae171-124">-NodeName</span><span class="sxs-lookup"><span data-stu-id="ae171-124">-NodeName</span></span>
<span data-ttu-id="ae171-125">整合執行時間節點名稱。</span><span class="sxs-lookup"><span data-stu-id="ae171-125">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae171-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae171-126">-ResourceGroupName</span></span>
<span data-ttu-id="ae171-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ae171-127">The resource group name.</span></span>

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

### <span data-ttu-id="ae171-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae171-128">-ResourceId</span></span>
<span data-ttu-id="ae171-129">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ae171-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ae171-130">-確認</span><span class="sxs-lookup"><span data-stu-id="ae171-130">-Confirm</span></span>
<span data-ttu-id="ae171-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ae171-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae171-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae171-132">-WhatIf</span></span>
<span data-ttu-id="ae171-133">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ae171-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="ae171-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae171-134">CommonParameters</span></span>
<span data-ttu-id="ae171-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ae171-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae171-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ae171-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae171-137">輸入</span><span class="sxs-lookup"><span data-stu-id="ae171-137">INPUTS</span></span>

### <span data-ttu-id="ae171-138">System.object</span><span class="sxs-lookup"><span data-stu-id="ae171-138">System.String</span></span>

### <span data-ttu-id="ae171-139">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="ae171-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="ae171-140">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="ae171-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="ae171-141">輸出</span><span class="sxs-lookup"><span data-stu-id="ae171-141">OUTPUTS</span></span>

### <span data-ttu-id="ae171-142">System.void</span><span class="sxs-lookup"><span data-stu-id="ae171-142">System.Void</span></span>

## <span data-ttu-id="ae171-143">筆記</span><span class="sxs-lookup"><span data-stu-id="ae171-143">NOTES</span></span>

## <span data-ttu-id="ae171-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="ae171-144">RELATED LINKS</span></span>
