---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 11d87742e34ae387f765551f93add5a1c300421a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906718"
---
# <span data-ttu-id="0aa48-101">New-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="0aa48-101">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="0aa48-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0aa48-102">SYNOPSIS</span></span>
<span data-ttu-id="0aa48-103">重新產生自我託管的整合執行時間金鑰。</span><span class="sxs-lookup"><span data-stu-id="0aa48-103">Regenerate self-hosted integration runtime key.</span></span>

## <span data-ttu-id="0aa48-104">語法</span><span class="sxs-lookup"><span data-stu-id="0aa48-104">SYNTAX</span></span>

### <span data-ttu-id="0aa48-105">By方能RuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="0aa48-105">ByIntegrationRuntimeName (Default)</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0aa48-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0aa48-106">ByResourceId</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0aa48-107">By方能RuntimeObject</span><span class="sxs-lookup"><span data-stu-id="0aa48-107">ByIntegrationRuntimeObject</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0aa48-108">描述</span><span class="sxs-lookup"><span data-stu-id="0aa48-108">DESCRIPTION</span></span>
<span data-ttu-id="0aa48-109">Cmdlet **New-AzDataFactoryV2 RuntimeRuntimeKey** 會以 KeyName' 參數指定的金鑰名稱重新產生整合執行時間金鑰。</span><span class="sxs-lookup"><span data-stu-id="0aa48-109">The cmdlet **New-AzDataFactoryV2IntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="0aa48-110">上一個按鍵無效。</span><span class="sxs-lookup"><span data-stu-id="0aa48-110">The previous key will is invalid.</span></span>

## <span data-ttu-id="0aa48-111">例子</span><span class="sxs-lookup"><span data-stu-id="0aa48-111">EXAMPLES</span></span>

### <span data-ttu-id="0aa48-112">範例 1：產生整合執行時間的新金鑰</span><span class="sxs-lookup"><span data-stu-id="0aa48-112">Example 1: Generate a new key for an integration runtime</span></span>
```
PS C:\> New-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -KeyName authKey2

AuthKey1 AuthKey2
-------- --------
         IR@89895504-f647-48fd-8dd3-42fa556d67e3@***
```

<span data-ttu-id="0aa48-113">Cmdlet 會針對名為'test-selfhost-ir'的整合執行時間重新產生 Key 'authKey2'。</span><span class="sxs-lookup"><span data-stu-id="0aa48-113">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="0aa48-114">參數</span><span class="sxs-lookup"><span data-stu-id="0aa48-114">PARAMETERS</span></span>

### <span data-ttu-id="0aa48-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0aa48-115">-DataFactoryName</span></span>
<span data-ttu-id="0aa48-116">資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="0aa48-116">The data factory name.</span></span>

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

### <span data-ttu-id="0aa48-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0aa48-117">-DefaultProfile</span></span>
<span data-ttu-id="0aa48-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0aa48-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0aa48-119">-強制</span><span class="sxs-lookup"><span data-stu-id="0aa48-119">-Force</span></span>
<span data-ttu-id="0aa48-120">執行 Cmdlet 而不提示確認。</span><span class="sxs-lookup"><span data-stu-id="0aa48-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="0aa48-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0aa48-121">-InputObject</span></span>
<span data-ttu-id="0aa48-122">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="0aa48-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="0aa48-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="0aa48-123">-KeyName</span></span>
<span data-ttu-id="0aa48-124">自我託管整合執行時間的驗證金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="0aa48-124">The authentication key name of the self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AuthKey1, AuthKey2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa48-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="0aa48-125">-Name</span></span>
<span data-ttu-id="0aa48-126">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="0aa48-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="0aa48-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0aa48-127">-ResourceGroupName</span></span>
<span data-ttu-id="0aa48-128">資源組名。</span><span class="sxs-lookup"><span data-stu-id="0aa48-128">The resource group name.</span></span>

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

### <span data-ttu-id="0aa48-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0aa48-129">-ResourceId</span></span>
<span data-ttu-id="0aa48-130">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0aa48-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0aa48-131">-確認</span><span class="sxs-lookup"><span data-stu-id="0aa48-131">-Confirm</span></span>
<span data-ttu-id="0aa48-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0aa48-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0aa48-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0aa48-133">-WhatIf</span></span>
<span data-ttu-id="0aa48-134">顯示如果 Cmdlet 執行，但不執行 Cmdlet 會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0aa48-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="0aa48-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aa48-135">CommonParameters</span></span>
<span data-ttu-id="0aa48-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0aa48-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aa48-137">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="0aa48-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aa48-138">輸入</span><span class="sxs-lookup"><span data-stu-id="0aa48-138">INPUTS</span></span>

### <span data-ttu-id="0aa48-139">System.String</span><span class="sxs-lookup"><span data-stu-id="0aa48-139">System.String</span></span>

### <span data-ttu-id="0aa48-140">Microsoft.Azure.Commands.DataFactoryV2.models.PSFactorRuntime</span><span class="sxs-lookup"><span data-stu-id="0aa48-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="0aa48-141">輸出</span><span class="sxs-lookup"><span data-stu-id="0aa48-141">OUTPUTS</span></span>

### <span data-ttu-id="0aa48-142">Microsoft.Azure.Commands.DataFactoryV2.models.PSFactorRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="0aa48-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="0aa48-143">筆記</span><span class="sxs-lookup"><span data-stu-id="0aa48-143">NOTES</span></span>

## <span data-ttu-id="0aa48-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="0aa48-144">RELATED LINKS</span></span>

[<span data-ttu-id="0aa48-145">Get-AzDataFactoryV2FactoryRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="0aa48-145">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()
