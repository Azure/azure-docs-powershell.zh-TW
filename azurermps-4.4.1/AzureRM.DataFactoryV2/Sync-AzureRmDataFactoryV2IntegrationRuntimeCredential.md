---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 63889ce74af1051211a579d1af7cc54be14822f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623671"
---
# <span data-ttu-id="a1d9c-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="a1d9c-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span></span>

## <span data-ttu-id="a1d9c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a1d9c-102">SYNOPSIS</span></span>
<span data-ttu-id="a1d9c-103">在整合執行時間節點之間同步處理認證。</span><span class="sxs-lookup"><span data-stu-id="a1d9c-103">Synchronizes credentials among integration runtime nodes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1d9c-104">句法</span><span class="sxs-lookup"><span data-stu-id="a1d9c-104">SYNTAX</span></span>

### <span data-ttu-id="a1d9c-105">ByIntegrationRuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="a1d9c-105">ByIntegrationRuntimeName (Default)</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a1d9c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a1d9c-106">ByResourceId</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a1d9c-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="a1d9c-107">ByIntegrationRuntimeObject</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-InputObject] <PSIntegrationRuntime>
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="a1d9c-108">說明</span><span class="sxs-lookup"><span data-stu-id="a1d9c-108">DESCRIPTION</span></span>
<span data-ttu-id="a1d9c-109">**AzureRmDataFactoryV2IntegrationRuntimeCredential** Cmdlet 會同步處理整合執行時間節點中的內部部署認證，這會強制在所有節點中都有相同的認證。</span><span class="sxs-lookup"><span data-stu-id="a1d9c-109">The **Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="a1d9c-110">示例</span><span class="sxs-lookup"><span data-stu-id="a1d9c-110">EXAMPLES</span></span>

### <span data-ttu-id="a1d9c-111">範例1：同步處理整合執行時間認證</span><span class="sxs-lookup"><span data-stu-id="a1d9c-111">Example 1: Sync an integration runtime credential</span></span>
```
PS C:\> Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="a1d9c-112">這個 Cmdlet 會同步處理整合執行時間節點之間的認證。</span><span class="sxs-lookup"><span data-stu-id="a1d9c-112">The cmdlet synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="a1d9c-113">參數</span><span class="sxs-lookup"><span data-stu-id="a1d9c-113">PARAMETERS</span></span>

### <span data-ttu-id="a1d9c-114">-確認</span><span class="sxs-lookup"><span data-stu-id="a1d9c-114">-Confirm</span></span>
<span data-ttu-id="a1d9c-115">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a1d9c-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1d9c-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a1d9c-116">-DataFactoryName</span></span>
<span data-ttu-id="a1d9c-117">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="a1d9c-117">The data factory name.</span></span>

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

### <span data-ttu-id="a1d9c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a1d9c-118">-Force</span></span>
<span data-ttu-id="a1d9c-119">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a1d9c-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="a1d9c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1d9c-120">-InputObject</span></span>
<span data-ttu-id="a1d9c-121">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="a1d9c-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="a1d9c-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="a1d9c-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="a1d9c-123">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="a1d9c-123">The integration runtime name.</span></span>

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

### <span data-ttu-id="a1d9c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1d9c-124">-ResourceGroupName</span></span>
<span data-ttu-id="a1d9c-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1d9c-125">The resource group name.</span></span>

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

### <span data-ttu-id="a1d9c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1d9c-126">-ResourceId</span></span>
<span data-ttu-id="a1d9c-127">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a1d9c-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="a1d9c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1d9c-128">-WhatIf</span></span>
<span data-ttu-id="a1d9c-129">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a1d9c-129">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="a1d9c-130">輸入</span><span class="sxs-lookup"><span data-stu-id="a1d9c-130">INPUTS</span></span>

### <span data-ttu-id="a1d9c-131">System.object</span><span class="sxs-lookup"><span data-stu-id="a1d9c-131">System.String</span></span>
<span data-ttu-id="a1d9c-132">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="a1d9c-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>


## <span data-ttu-id="a1d9c-133">輸出</span><span class="sxs-lookup"><span data-stu-id="a1d9c-133">OUTPUTS</span></span>

### <span data-ttu-id="a1d9c-134">System.object</span><span class="sxs-lookup"><span data-stu-id="a1d9c-134">System.Object</span></span>

## <span data-ttu-id="a1d9c-135">筆記</span><span class="sxs-lookup"><span data-stu-id="a1d9c-135">NOTES</span></span>

## <span data-ttu-id="a1d9c-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="a1d9c-136">RELATED LINKS</span></span>
