---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
ms.openlocfilehash: e89f4c69996f5527c49db72f3185e5a126b348c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447122"
---
# <span data-ttu-id="10759-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="10759-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span></span>

## <span data-ttu-id="10759-102">摘要</span><span class="sxs-lookup"><span data-stu-id="10759-102">SYNOPSIS</span></span>
<span data-ttu-id="10759-103">在整合執行時間節點之間同步處理認證。</span><span class="sxs-lookup"><span data-stu-id="10759-103">Synchronizes credentials among integration runtime nodes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10759-104">句法</span><span class="sxs-lookup"><span data-stu-id="10759-104">SYNTAX</span></span>

### <span data-ttu-id="10759-105">ByIntegrationRuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="10759-105">ByIntegrationRuntimeName (Default)</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10759-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="10759-106">ByResourceId</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10759-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="10759-107">ByIntegrationRuntimeObject</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10759-108">說明</span><span class="sxs-lookup"><span data-stu-id="10759-108">DESCRIPTION</span></span>
<span data-ttu-id="10759-109">**AzureRmDataFactoryV2IntegrationRuntimeCredential** Cmdlet 會同步處理整合執行時間節點中的內部部署認證，這會強制在所有節點中都有相同的認證。</span><span class="sxs-lookup"><span data-stu-id="10759-109">The **Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="10759-110">示例</span><span class="sxs-lookup"><span data-stu-id="10759-110">EXAMPLES</span></span>

### <span data-ttu-id="10759-111">範例1：同步處理整合執行時間認證</span><span class="sxs-lookup"><span data-stu-id="10759-111">Example 1: Sync an integration runtime credential</span></span>
```
PS C:\> Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="10759-112">這個 Cmdlet 會同步處理整合執行時間節點之間的認證。</span><span class="sxs-lookup"><span data-stu-id="10759-112">The cmdlet synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="10759-113">參數</span><span class="sxs-lookup"><span data-stu-id="10759-113">PARAMETERS</span></span>

### <span data-ttu-id="10759-114">-確認</span><span class="sxs-lookup"><span data-stu-id="10759-114">-Confirm</span></span>
<span data-ttu-id="10759-115">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="10759-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10759-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="10759-116">-DataFactoryName</span></span>
<span data-ttu-id="10759-117">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="10759-117">The data factory name.</span></span>

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

### <span data-ttu-id="10759-118">-Force</span><span class="sxs-lookup"><span data-stu-id="10759-118">-Force</span></span>
<span data-ttu-id="10759-119">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="10759-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="10759-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10759-120">-InputObject</span></span>
<span data-ttu-id="10759-121">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="10759-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="10759-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="10759-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="10759-123">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="10759-123">The integration runtime name.</span></span>

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

### <span data-ttu-id="10759-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10759-124">-ResourceGroupName</span></span>
<span data-ttu-id="10759-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="10759-125">The resource group name.</span></span>

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

### <span data-ttu-id="10759-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10759-126">-ResourceId</span></span>
<span data-ttu-id="10759-127">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="10759-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="10759-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10759-128">-WhatIf</span></span>
<span data-ttu-id="10759-129">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="10759-129">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="10759-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10759-130">-DefaultProfile</span></span>
<span data-ttu-id="10759-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="10759-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10759-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10759-132">CommonParameters</span></span>
<span data-ttu-id="10759-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="10759-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10759-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="10759-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10759-135">輸入</span><span class="sxs-lookup"><span data-stu-id="10759-135">INPUTS</span></span>

### <span data-ttu-id="10759-136">System.object</span><span class="sxs-lookup"><span data-stu-id="10759-136">System.String</span></span>
<span data-ttu-id="10759-137">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="10759-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="10759-138">輸出</span><span class="sxs-lookup"><span data-stu-id="10759-138">OUTPUTS</span></span>

### <span data-ttu-id="10759-139">System.object</span><span class="sxs-lookup"><span data-stu-id="10759-139">System.Object</span></span>

## <span data-ttu-id="10759-140">筆記</span><span class="sxs-lookup"><span data-stu-id="10759-140">NOTES</span></span>

## <span data-ttu-id="10759-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="10759-141">RELATED LINKS</span></span>

