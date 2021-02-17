---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 44439d49fc89f00abaef904e80112d076121890f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100408639"
---
# <span data-ttu-id="c1149-101">Set-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="c1149-101">Set-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="c1149-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c1149-102">SYNOPSIS</span></span>
<span data-ttu-id="c1149-103">在 Data Factory 中建立資料流程。</span><span class="sxs-lookup"><span data-stu-id="c1149-103">Creates a data flow in Data Factory.</span></span>

## <span data-ttu-id="c1149-104">語法</span><span class="sxs-lookup"><span data-stu-id="c1149-104">SYNTAX</span></span>

### <span data-ttu-id="c1149-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="c1149-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2DataFlow [-Name] <String> [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c1149-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c1149-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2DataFlow [-DefinitionFile] <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1149-107">描述</span><span class="sxs-lookup"><span data-stu-id="c1149-107">DESCRIPTION</span></span>
<span data-ttu-id="c1149-108">Cmdlet Set-AzDataFactoryV2DataFlow建立資料流程，或更新 Azure Data Factory 中現有的資料流程。</span><span class="sxs-lookup"><span data-stu-id="c1149-108">The Set-AzDataFactoryV2DataFlow cmdlet creates a data flow or updates an existing data flow in Azure Data Factory.</span></span>

## <span data-ttu-id="c1149-109">例子</span><span class="sxs-lookup"><span data-stu-id="c1149-109">EXAMPLES</span></span>

### <span data-ttu-id="c1149-110">範例 1：建立資料流程</span><span class="sxs-lookup"><span data-stu-id="c1149-110">Example 1: Create a data flow</span></span>
```powershell
PS C:\> Set-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "TaxiDemo1" -DefinitionFile "C:\\samples\\WikiSample\\TaxiDemo1.json"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="c1149-111">此命令在名稱為 WikiADF 的資料工廠中，建立名為一個名為一個以一個資料流程程命名的一個資料流程程。</span><span class="sxs-lookup"><span data-stu-id="c1149-111">This command creates a data flow named TaxiDemo1 in the data factory named WikiADF.</span></span>
<span data-ttu-id="c1149-112">命令以檔案中資料TaxiDemo1.js的基礎。</span><span class="sxs-lookup"><span data-stu-id="c1149-112">The command bases the data flow on information in the TaxiDemo1.json file.</span></span>

## <span data-ttu-id="c1149-113">參數</span><span class="sxs-lookup"><span data-stu-id="c1149-113">PARAMETERS</span></span>

### <span data-ttu-id="c1149-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c1149-114">-DataFactoryName</span></span>
<span data-ttu-id="c1149-115">資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="c1149-115">The data factory name.</span></span>

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

### <span data-ttu-id="c1149-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1149-116">-DefaultProfile</span></span>
<span data-ttu-id="c1149-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c1149-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1149-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="c1149-118">-DefinitionFile</span></span>
<span data-ttu-id="c1149-119">JSON 檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="c1149-119">The JSON file path.</span></span>

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

### <span data-ttu-id="c1149-120">-強制</span><span class="sxs-lookup"><span data-stu-id="c1149-120">-Force</span></span>
<span data-ttu-id="c1149-121">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="c1149-121">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="c1149-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="c1149-122">-Name</span></span>
<span data-ttu-id="c1149-123">資料流程名稱。</span><span class="sxs-lookup"><span data-stu-id="c1149-123">The data flow name.</span></span>

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

### <span data-ttu-id="c1149-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1149-124">-ResourceGroupName</span></span>
<span data-ttu-id="c1149-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="c1149-125">The resource group name.</span></span>

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

### <span data-ttu-id="c1149-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1149-126">-ResourceId</span></span>
<span data-ttu-id="c1149-127">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c1149-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="c1149-128">-確認</span><span class="sxs-lookup"><span data-stu-id="c1149-128">-Confirm</span></span>
<span data-ttu-id="c1149-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c1149-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1149-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1149-130">-WhatIf</span></span>
<span data-ttu-id="c1149-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c1149-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1149-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c1149-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1149-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1149-133">CommonParameters</span></span>
<span data-ttu-id="c1149-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c1149-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1149-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c1149-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1149-136">輸入</span><span class="sxs-lookup"><span data-stu-id="c1149-136">INPUTS</span></span>

### <span data-ttu-id="c1149-137">System.String</span><span class="sxs-lookup"><span data-stu-id="c1149-137">System.String</span></span>

## <span data-ttu-id="c1149-138">輸出</span><span class="sxs-lookup"><span data-stu-id="c1149-138">OUTPUTS</span></span>

### <span data-ttu-id="c1149-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="c1149-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="c1149-140">筆記</span><span class="sxs-lookup"><span data-stu-id="c1149-140">NOTES</span></span>
<span data-ttu-id="c1149-141">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="c1149-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c1149-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="c1149-142">RELATED LINKS</span></span>


