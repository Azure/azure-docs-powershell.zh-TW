---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 42d9de3f23f1aca904aa0f42722217d0b9bf8a3a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798817"
---
# <span data-ttu-id="a01ea-101">Set-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="a01ea-101">Set-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="a01ea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a01ea-102">SYNOPSIS</span></span>
<span data-ttu-id="a01ea-103">在資料工廠中建立資料流程。</span><span class="sxs-lookup"><span data-stu-id="a01ea-103">Creates a data flow in Data Factory.</span></span>

## <span data-ttu-id="a01ea-104">句法</span><span class="sxs-lookup"><span data-stu-id="a01ea-104">SYNTAX</span></span>

### <span data-ttu-id="a01ea-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="a01ea-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2DataFlow [-Name] <String> [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a01ea-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a01ea-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2DataFlow [-DefinitionFile] <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a01ea-107">說明</span><span class="sxs-lookup"><span data-stu-id="a01ea-107">DESCRIPTION</span></span>
<span data-ttu-id="a01ea-108">Set-AzDataFactoryV2DataFlow Cmdlet 會建立資料流程程或更新 Azure 資料工廠中現有的資料流程。</span><span class="sxs-lookup"><span data-stu-id="a01ea-108">The Set-AzDataFactoryV2DataFlow cmdlet creates a data flow or updates an existing data flow in Azure Data Factory.</span></span>

## <span data-ttu-id="a01ea-109">示例</span><span class="sxs-lookup"><span data-stu-id="a01ea-109">EXAMPLES</span></span>

### <span data-ttu-id="a01ea-110">範例1：建立資料流程程</span><span class="sxs-lookup"><span data-stu-id="a01ea-110">Example 1: Create a data flow</span></span>
```powershell
PS C:\> Set-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "TaxiDemo1" -DefinitionFile "C:\\samples\\WikiSample\\TaxiDemo1.json"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="a01ea-111">這個命令會在名為 WikiADF 的資料工廠中建立名為 TaxiDemo1 的資料流程。</span><span class="sxs-lookup"><span data-stu-id="a01ea-111">This command creates a data flow named TaxiDemo1 in the data factory named WikiADF.</span></span>
<span data-ttu-id="a01ea-112">此命令會根據檔案中 TaxiDemo1.js的資訊來控制資料流程。</span><span class="sxs-lookup"><span data-stu-id="a01ea-112">The command bases the data flow on information in the TaxiDemo1.json file.</span></span>

## <span data-ttu-id="a01ea-113">參數</span><span class="sxs-lookup"><span data-stu-id="a01ea-113">PARAMETERS</span></span>

### <span data-ttu-id="a01ea-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a01ea-114">-DataFactoryName</span></span>
<span data-ttu-id="a01ea-115">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="a01ea-115">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a01ea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a01ea-116">-DefaultProfile</span></span>
<span data-ttu-id="a01ea-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a01ea-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a01ea-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="a01ea-118">-DefinitionFile</span></span>
<span data-ttu-id="a01ea-119">JSON 檔路徑。</span><span class="sxs-lookup"><span data-stu-id="a01ea-119">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01ea-120">-Force</span><span class="sxs-lookup"><span data-stu-id="a01ea-120">-Force</span></span>
<span data-ttu-id="a01ea-121">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="a01ea-121">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="a01ea-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="a01ea-122">-Name</span></span>
<span data-ttu-id="a01ea-123">資料流程程名稱。</span><span class="sxs-lookup"><span data-stu-id="a01ea-123">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFlowName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a01ea-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a01ea-124">-ResourceGroupName</span></span>
<span data-ttu-id="a01ea-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a01ea-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a01ea-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a01ea-126">-ResourceId</span></span>
<span data-ttu-id="a01ea-127">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a01ea-127">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a01ea-128">-確認</span><span class="sxs-lookup"><span data-stu-id="a01ea-128">-Confirm</span></span>
<span data-ttu-id="a01ea-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a01ea-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a01ea-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a01ea-130">-WhatIf</span></span>
<span data-ttu-id="a01ea-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a01ea-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a01ea-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a01ea-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a01ea-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a01ea-133">CommonParameters</span></span>
<span data-ttu-id="a01ea-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a01ea-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a01ea-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a01ea-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a01ea-136">輸入</span><span class="sxs-lookup"><span data-stu-id="a01ea-136">INPUTS</span></span>

### <span data-ttu-id="a01ea-137">System.object</span><span class="sxs-lookup"><span data-stu-id="a01ea-137">System.String</span></span>

## <span data-ttu-id="a01ea-138">輸出</span><span class="sxs-lookup"><span data-stu-id="a01ea-138">OUTPUTS</span></span>

### <span data-ttu-id="a01ea-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="a01ea-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="a01ea-140">筆記</span><span class="sxs-lookup"><span data-stu-id="a01ea-140">NOTES</span></span>
<span data-ttu-id="a01ea-141">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="a01ea-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a01ea-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="a01ea-142">RELATED LINKS</span></span>

[<span data-ttu-id="a01ea-143">AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="a01ea-143">Get-AzDataFactoryDataFlow</span></span>](./Get-AzDataFactoryDataFlow.md)

[<span data-ttu-id="a01ea-144">移除-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="a01ea-144">Remove-AzDataFactoryDataFlow</span></span>](./Remove-AzDataFactoryDataFlow.md)
