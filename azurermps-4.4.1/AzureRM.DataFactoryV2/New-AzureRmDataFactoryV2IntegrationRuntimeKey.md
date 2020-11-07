---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2IntegrationRuntimeKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 166bae99bebbc5a1b1c25ffc79faa3a1f7254bbc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623672"
---
# <span data-ttu-id="cf344-101">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="cf344-101">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="cf344-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cf344-102">SYNOPSIS</span></span>
<span data-ttu-id="cf344-103">重新產生自託管的整合執行時間金鑰。</span><span class="sxs-lookup"><span data-stu-id="cf344-103">Regenerate self-hosted integration runtime key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf344-104">句法</span><span class="sxs-lookup"><span data-stu-id="cf344-104">SYNTAX</span></span>

### <span data-ttu-id="cf344-105">ByIntegrationRuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="cf344-105">ByIntegrationRuntimeName (Default)</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="cf344-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cf344-106">ByResourceId</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-ResourceId] <String> [-WhatIf]
 [-Confirm]
```

### <span data-ttu-id="cf344-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="cf344-107">ByIntegrationRuntimeObject</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force]
 [-InputObject] <PSIntegrationRuntime> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="cf344-108">說明</span><span class="sxs-lookup"><span data-stu-id="cf344-108">DESCRIPTION</span></span>
<span data-ttu-id="cf344-109">Cmdlet **AzureRmDataFactoryV2IntegrationRuntimeKey** 會再生整合執行時間金鑰，並使用由 "KeyName" 參數指定的金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="cf344-109">The cmdlet **New-AzureRmDataFactoryV2IntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="cf344-110">前一個金鑰將無效。</span><span class="sxs-lookup"><span data-stu-id="cf344-110">The previous key will is invalid.</span></span>

## <span data-ttu-id="cf344-111">示例</span><span class="sxs-lookup"><span data-stu-id="cf344-111">EXAMPLES</span></span>

### <span data-ttu-id="cf344-112">範例1：為整合執行時間產生新的金鑰</span><span class="sxs-lookup"><span data-stu-id="cf344-112">Example 1: Generate a new key for an integration runtime</span></span>
```
PS C:\> New-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -KeyName authKey2

AuthKey1 AuthKey2
-------- --------
         IR@89895504-f647-48fd-8dd3-42fa556d67e3@***
```

<span data-ttu-id="cf344-113">這個 Cmdlet 會為集成執行時間（名為「test-selfhost-ir」）重新產生金鑰 ' authKey2」。</span><span class="sxs-lookup"><span data-stu-id="cf344-113">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="cf344-114">參數</span><span class="sxs-lookup"><span data-stu-id="cf344-114">PARAMETERS</span></span>

### <span data-ttu-id="cf344-115">-確認</span><span class="sxs-lookup"><span data-stu-id="cf344-115">-Confirm</span></span>
<span data-ttu-id="cf344-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cf344-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf344-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="cf344-117">-DataFactoryName</span></span>
<span data-ttu-id="cf344-118">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="cf344-118">The data factory name.</span></span>

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

### <span data-ttu-id="cf344-119">-Force</span><span class="sxs-lookup"><span data-stu-id="cf344-119">-Force</span></span>
<span data-ttu-id="cf344-120">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cf344-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="cf344-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf344-121">-InputObject</span></span>
<span data-ttu-id="cf344-122">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="cf344-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="cf344-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="cf344-123">-KeyName</span></span>
<span data-ttu-id="cf344-124">自託管整合執行時間的驗證金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="cf344-124">The authentication key name of the self-hosted integration runtime.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AuthKey1, AuthKey2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf344-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="cf344-125">-Name</span></span>
<span data-ttu-id="cf344-126">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="cf344-126">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf344-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf344-127">-ResourceGroupName</span></span>
<span data-ttu-id="cf344-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf344-128">The resource group name.</span></span>

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

### <span data-ttu-id="cf344-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf344-129">-ResourceId</span></span>
<span data-ttu-id="cf344-130">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="cf344-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="cf344-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf344-131">-WhatIf</span></span>
<span data-ttu-id="cf344-132">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cf344-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="cf344-133">輸入</span><span class="sxs-lookup"><span data-stu-id="cf344-133">INPUTS</span></span>

### <span data-ttu-id="cf344-134">System.object</span><span class="sxs-lookup"><span data-stu-id="cf344-134">System.String</span></span>
<span data-ttu-id="cf344-135">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="cf344-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>


## <span data-ttu-id="cf344-136">輸出</span><span class="sxs-lookup"><span data-stu-id="cf344-136">OUTPUTS</span></span>

### <span data-ttu-id="cf344-137">PSIntegrationRuntimeKeys 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="cf344-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>


## <span data-ttu-id="cf344-138">筆記</span><span class="sxs-lookup"><span data-stu-id="cf344-138">NOTES</span></span>

## <span data-ttu-id="cf344-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf344-139">RELATED LINKS</span></span>
[<span data-ttu-id="cf344-140">AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="cf344-140">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()
