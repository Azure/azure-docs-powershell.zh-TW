---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/sync-azdatafactoryv2integrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Sync-AzDataFactoryV2IntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Sync-AzDataFactoryV2IntegrationRuntimeCredential.md
ms.openlocfilehash: 40f6a6c5f446b23a92a2ca5c5c8c872297b2a81a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612886"
---
# <span data-ttu-id="f03ec-101">Sync-AzDataFactoryV2IntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="f03ec-101">Sync-AzDataFactoryV2IntegrationRuntimeCredential</span></span>

## <span data-ttu-id="f03ec-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f03ec-102">SYNOPSIS</span></span>
<span data-ttu-id="f03ec-103">在整合執行時間節點之間同步處理認證。</span><span class="sxs-lookup"><span data-stu-id="f03ec-103">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="f03ec-104">句法</span><span class="sxs-lookup"><span data-stu-id="f03ec-104">SYNTAX</span></span>

### <span data-ttu-id="f03ec-105">ByIntegrationRuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="f03ec-105">ByIntegrationRuntimeName (Default)</span></span>
```
Sync-AzDataFactoryV2IntegrationRuntimeCredential [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f03ec-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f03ec-106">ByResourceId</span></span>
```
Sync-AzDataFactoryV2IntegrationRuntimeCredential [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f03ec-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="f03ec-107">ByIntegrationRuntimeObject</span></span>
```
Sync-AzDataFactoryV2IntegrationRuntimeCredential [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f03ec-108">說明</span><span class="sxs-lookup"><span data-stu-id="f03ec-108">DESCRIPTION</span></span>
<span data-ttu-id="f03ec-109">**AzDataFactoryV2IntegrationRuntimeCredential** Cmdlet 會同步處理整合執行時間節點中的內部部署認證，這會強制在所有節點中都有相同的認證。</span><span class="sxs-lookup"><span data-stu-id="f03ec-109">The **Sync-AzDataFactoryV2IntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="f03ec-110">示例</span><span class="sxs-lookup"><span data-stu-id="f03ec-110">EXAMPLES</span></span>

### <span data-ttu-id="f03ec-111">範例1：同步處理整合執行時間認證</span><span class="sxs-lookup"><span data-stu-id="f03ec-111">Example 1: Sync an integration runtime credential</span></span>
```
PS C:\> Sync-AzDataFactoryV2IntegrationRuntimeCredential -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="f03ec-112">這個 Cmdlet 會同步處理整合執行時間節點之間的認證。</span><span class="sxs-lookup"><span data-stu-id="f03ec-112">The cmdlet synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="f03ec-113">參數</span><span class="sxs-lookup"><span data-stu-id="f03ec-113">PARAMETERS</span></span>

### <span data-ttu-id="f03ec-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f03ec-114">-DataFactoryName</span></span>
<span data-ttu-id="f03ec-115">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="f03ec-115">The data factory name.</span></span>

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

### <span data-ttu-id="f03ec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f03ec-116">-DefaultProfile</span></span>
<span data-ttu-id="f03ec-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f03ec-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f03ec-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f03ec-118">-Force</span></span>
<span data-ttu-id="f03ec-119">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f03ec-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="f03ec-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f03ec-120">-InputObject</span></span>
<span data-ttu-id="f03ec-121">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="f03ec-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="f03ec-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="f03ec-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="f03ec-123">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="f03ec-123">The integration runtime name.</span></span>

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

### <span data-ttu-id="f03ec-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f03ec-124">-ResourceGroupName</span></span>
<span data-ttu-id="f03ec-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f03ec-125">The resource group name.</span></span>

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

### <span data-ttu-id="f03ec-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f03ec-126">-ResourceId</span></span>
<span data-ttu-id="f03ec-127">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f03ec-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="f03ec-128">-確認</span><span class="sxs-lookup"><span data-stu-id="f03ec-128">-Confirm</span></span>
<span data-ttu-id="f03ec-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f03ec-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f03ec-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f03ec-130">-WhatIf</span></span>
<span data-ttu-id="f03ec-131">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f03ec-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="f03ec-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f03ec-132">CommonParameters</span></span>
<span data-ttu-id="f03ec-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f03ec-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f03ec-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f03ec-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f03ec-135">輸入</span><span class="sxs-lookup"><span data-stu-id="f03ec-135">INPUTS</span></span>

### <span data-ttu-id="f03ec-136">System.object</span><span class="sxs-lookup"><span data-stu-id="f03ec-136">System.String</span></span>

### <span data-ttu-id="f03ec-137">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="f03ec-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="f03ec-138">輸出</span><span class="sxs-lookup"><span data-stu-id="f03ec-138">OUTPUTS</span></span>

### <span data-ttu-id="f03ec-139">System.void</span><span class="sxs-lookup"><span data-stu-id="f03ec-139">System.Void</span></span>

## <span data-ttu-id="f03ec-140">筆記</span><span class="sxs-lookup"><span data-stu-id="f03ec-140">NOTES</span></span>

## <span data-ttu-id="f03ec-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="f03ec-141">RELATED LINKS</span></span>
