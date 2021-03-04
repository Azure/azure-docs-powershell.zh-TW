---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 72b00b855bcc50df2766a6b8d0315780aaa64ecf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916634"
---
# <span data-ttu-id="4e02e-101">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4e02e-101">Remove-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="4e02e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4e02e-102">SYNOPSIS</span></span>
<span data-ttu-id="4e02e-103">移除整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="4e02e-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="4e02e-104">語法</span><span class="sxs-lookup"><span data-stu-id="4e02e-104">SYNTAX</span></span>

### <span data-ttu-id="4e02e-105">By方能RuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="4e02e-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e02e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4e02e-106">ByResourceId</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e02e-107">By方能RuntimeObject</span><span class="sxs-lookup"><span data-stu-id="4e02e-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4e02e-108">描述</span><span class="sxs-lookup"><span data-stu-id="4e02e-108">DESCRIPTION</span></span>
<span data-ttu-id="4e02e-109">Cmdlet Remove-AzDataFactoryV2IntegrationRuntime移除整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="4e02e-109">The Remove-AzDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="4e02e-110">例子</span><span class="sxs-lookup"><span data-stu-id="4e02e-110">EXAMPLES</span></span>

### <span data-ttu-id="4e02e-111">範例 1：移除整合執行時間</span><span class="sxs-lookup"><span data-stu-id="4e02e-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="4e02e-112">此命令會從名為"test-df"的資料工廠移除名為"test-reserved-ir"的整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="4e02e-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="4e02e-113">此命令會返回 $True。</span><span class="sxs-lookup"><span data-stu-id="4e02e-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="4e02e-114">參數</span><span class="sxs-lookup"><span data-stu-id="4e02e-114">PARAMETERS</span></span>

### <span data-ttu-id="4e02e-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4e02e-115">-DataFactoryName</span></span>
<span data-ttu-id="4e02e-116">資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="4e02e-116">The data factory name.</span></span>

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

### <span data-ttu-id="4e02e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e02e-117">-DefaultProfile</span></span>
<span data-ttu-id="4e02e-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4e02e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e02e-119">-強制</span><span class="sxs-lookup"><span data-stu-id="4e02e-119">-Force</span></span>
<span data-ttu-id="4e02e-120">執行 Cmdlet 而不提示確認。</span><span class="sxs-lookup"><span data-stu-id="4e02e-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="4e02e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e02e-121">-InputObject</span></span>
<span data-ttu-id="4e02e-122">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="4e02e-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="4e02e-123">-LinkedDataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4e02e-123">-LinkedDataFactoryName</span></span>
<span data-ttu-id="4e02e-124">連結的資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="4e02e-124">The linked data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e02e-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="4e02e-125">-Name</span></span>
<span data-ttu-id="4e02e-126">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="4e02e-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="4e02e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e02e-127">-ResourceGroupName</span></span>
<span data-ttu-id="4e02e-128">資源組名。</span><span class="sxs-lookup"><span data-stu-id="4e02e-128">The resource group name.</span></span>

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

### <span data-ttu-id="4e02e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e02e-129">-ResourceId</span></span>
<span data-ttu-id="4e02e-130">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4e02e-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="4e02e-131">-確認</span><span class="sxs-lookup"><span data-stu-id="4e02e-131">-Confirm</span></span>
<span data-ttu-id="4e02e-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4e02e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e02e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e02e-133">-WhatIf</span></span>
<span data-ttu-id="4e02e-134">顯示如果 Cmdlet 執行，但不執行 Cmdlet 會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4e02e-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="4e02e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e02e-135">CommonParameters</span></span>
<span data-ttu-id="4e02e-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4e02e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e02e-137">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="4e02e-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e02e-138">輸入</span><span class="sxs-lookup"><span data-stu-id="4e02e-138">INPUTS</span></span>

### <span data-ttu-id="4e02e-139">System.String</span><span class="sxs-lookup"><span data-stu-id="4e02e-139">System.String</span></span>

### <span data-ttu-id="4e02e-140">Microsoft.Azure.Commands.DataFactoryV2.models.PSFactorRuntime</span><span class="sxs-lookup"><span data-stu-id="4e02e-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="4e02e-141">輸出</span><span class="sxs-lookup"><span data-stu-id="4e02e-141">OUTPUTS</span></span>

### <span data-ttu-id="4e02e-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="4e02e-142">System.Void</span></span>

## <span data-ttu-id="4e02e-143">筆記</span><span class="sxs-lookup"><span data-stu-id="4e02e-143">NOTES</span></span>
<span data-ttu-id="4e02e-144">關鍵字：azure、azurerm、arm、資源、管理、管理員、資料、專案、複製、活動、整合執行時間</span><span class="sxs-lookup"><span data-stu-id="4e02e-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="4e02e-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e02e-145">RELATED LINKS</span></span>

[<span data-ttu-id="4e02e-146">Set-AzDataFactoryV2FactoryRuntime</span><span class="sxs-lookup"><span data-stu-id="4e02e-146">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="4e02e-147">Get-AzDataFactoryV2FactoryRuntime</span><span class="sxs-lookup"><span data-stu-id="4e02e-147">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

