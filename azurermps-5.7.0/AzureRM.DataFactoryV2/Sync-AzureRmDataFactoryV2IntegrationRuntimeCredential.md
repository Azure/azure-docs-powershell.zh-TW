---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/sync-azurermdatafactoryv2integrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
ms.openlocfilehash: 11619cf9d5699b626032f82efbc9674713076ece
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448711"
---
# <span data-ttu-id="15dcc-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="15dcc-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span></span>

## <span data-ttu-id="15dcc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="15dcc-102">SYNOPSIS</span></span>
<span data-ttu-id="15dcc-103">在整合執行時間節點之間同步處理認證。</span><span class="sxs-lookup"><span data-stu-id="15dcc-103">Synchronizes credentials among integration runtime nodes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15dcc-104">句法</span><span class="sxs-lookup"><span data-stu-id="15dcc-104">SYNTAX</span></span>

### <span data-ttu-id="15dcc-105">ByIntegrationRuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="15dcc-105">ByIntegrationRuntimeName (Default)</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15dcc-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="15dcc-106">ByResourceId</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15dcc-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="15dcc-107">ByIntegrationRuntimeObject</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15dcc-108">說明</span><span class="sxs-lookup"><span data-stu-id="15dcc-108">DESCRIPTION</span></span>
<span data-ttu-id="15dcc-109">**AzureRmDataFactoryV2IntegrationRuntimeCredential** Cmdlet 會同步處理整合執行時間節點中的內部部署認證，這會強制在所有節點中都有相同的認證。</span><span class="sxs-lookup"><span data-stu-id="15dcc-109">The **Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="15dcc-110">示例</span><span class="sxs-lookup"><span data-stu-id="15dcc-110">EXAMPLES</span></span>

### <span data-ttu-id="15dcc-111">範例1：同步處理整合執行時間認證</span><span class="sxs-lookup"><span data-stu-id="15dcc-111">Example 1: Sync an integration runtime credential</span></span>
```
PS C:\> Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="15dcc-112">這個 Cmdlet 會同步處理整合執行時間節點之間的認證。</span><span class="sxs-lookup"><span data-stu-id="15dcc-112">The cmdlet synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="15dcc-113">參數</span><span class="sxs-lookup"><span data-stu-id="15dcc-113">PARAMETERS</span></span>

### <span data-ttu-id="15dcc-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="15dcc-114">-DataFactoryName</span></span>
<span data-ttu-id="15dcc-115">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="15dcc-115">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15dcc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15dcc-116">-DefaultProfile</span></span>
<span data-ttu-id="15dcc-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="15dcc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15dcc-118">-Force</span><span class="sxs-lookup"><span data-stu-id="15dcc-118">-Force</span></span>
<span data-ttu-id="15dcc-119">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="15dcc-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="15dcc-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15dcc-120">-InputObject</span></span>
<span data-ttu-id="15dcc-121">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="15dcc-121">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15dcc-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="15dcc-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="15dcc-123">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="15dcc-123">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15dcc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15dcc-124">-ResourceGroupName</span></span>
<span data-ttu-id="15dcc-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="15dcc-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15dcc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="15dcc-126">-ResourceId</span></span>
<span data-ttu-id="15dcc-127">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="15dcc-127">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15dcc-128">-確認</span><span class="sxs-lookup"><span data-stu-id="15dcc-128">-Confirm</span></span>
<span data-ttu-id="15dcc-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="15dcc-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15dcc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15dcc-130">-WhatIf</span></span>
<span data-ttu-id="15dcc-131">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="15dcc-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15dcc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15dcc-132">CommonParameters</span></span>
<span data-ttu-id="15dcc-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="15dcc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15dcc-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="15dcc-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15dcc-135">輸入</span><span class="sxs-lookup"><span data-stu-id="15dcc-135">INPUTS</span></span>

### <span data-ttu-id="15dcc-136">System.object</span><span class="sxs-lookup"><span data-stu-id="15dcc-136">System.String</span></span>
<span data-ttu-id="15dcc-137">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="15dcc-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="15dcc-138">輸出</span><span class="sxs-lookup"><span data-stu-id="15dcc-138">OUTPUTS</span></span>

### <span data-ttu-id="15dcc-139">System.object</span><span class="sxs-lookup"><span data-stu-id="15dcc-139">System.Object</span></span>

## <span data-ttu-id="15dcc-140">筆記</span><span class="sxs-lookup"><span data-stu-id="15dcc-140">NOTES</span></span>

## <span data-ttu-id="15dcc-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="15dcc-141">RELATED LINKS</span></span>

