---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 7bd25d444a4277e2aa423026be551fab1c5f360e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100397861"
---
# <span data-ttu-id="aa903-101">Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="aa903-101">Get-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="aa903-102">簡介</span><span class="sxs-lookup"><span data-stu-id="aa903-102">SYNOPSIS</span></span>
<span data-ttu-id="aa903-103">在 Data Factory 中獲得資料流程相關資訊。</span><span class="sxs-lookup"><span data-stu-id="aa903-103">Gets information about data flows in Data Factory.</span></span>

## <span data-ttu-id="aa903-104">語法</span><span class="sxs-lookup"><span data-stu-id="aa903-104">SYNTAX</span></span>

### <span data-ttu-id="aa903-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="aa903-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa903-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="aa903-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa903-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="aa903-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlow [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aa903-108">描述</span><span class="sxs-lookup"><span data-stu-id="aa903-108">DESCRIPTION</span></span>
<span data-ttu-id="aa903-109">Cmdlet Get-AzDataFactoryV2DataFlow Azure Data Factory 中有關資料流程的資訊。</span><span class="sxs-lookup"><span data-stu-id="aa903-109">The Get-AzDataFactoryV2DataFlow cmdlet gets information about data flows in Azure Data Factory.</span></span>
<span data-ttu-id="aa903-110">如果您指定資料流程的名稱，此 Cmdlet 會獲得該資料流程的資訊。</span><span class="sxs-lookup"><span data-stu-id="aa903-110">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="aa903-111">如果您未指定名稱，此 Cmdlet 會獲得資料工廠中所有資料流量的資訊。</span><span class="sxs-lookup"><span data-stu-id="aa903-111">If you do not specify a name, this cmdlet gets information about all the data flows in the data factory.</span></span>

## <span data-ttu-id="aa903-112">例子</span><span class="sxs-lookup"><span data-stu-id="aa903-112">EXAMPLES</span></span>
### <span data-ttu-id="aa903-113">範例 1：取得所有資料流程的資訊</span><span class="sxs-lookup"><span data-stu-id="aa903-113">Example 1: Get information about all data flows</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow3                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="aa903-114">此命令會獲得名稱為 WikiADF 的資料工廠中所有資料流程的資訊。</span><span class="sxs-lookup"><span data-stu-id="aa903-114">This command gets information about all data flows in the data factory named WikiADF.</span></span>

### <span data-ttu-id="aa903-115">範例 2：取得特定資料流程的資訊</span><span class="sxs-lookup"><span data-stu-id="aa903-115">Example 2: Get information about a specific data flow</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "dataflow1"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="aa903-116">此命令會從名稱為 WikiADF 的資料工廠中，獲得名為 Dataflow1 的資料流程程相關資訊。</span><span class="sxs-lookup"><span data-stu-id="aa903-116">This command gets information about the data flow named dataflow1 in the data factory named WikiADF.</span></span>

## <span data-ttu-id="aa903-117">參數</span><span class="sxs-lookup"><span data-stu-id="aa903-117">PARAMETERS</span></span>

### <span data-ttu-id="aa903-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="aa903-118">-DataFactory</span></span>
<span data-ttu-id="aa903-119">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="aa903-119">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa903-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="aa903-120">-DataFactoryName</span></span>
<span data-ttu-id="aa903-121">資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="aa903-121">The data factory name.</span></span>

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

### <span data-ttu-id="aa903-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa903-122">-DefaultProfile</span></span>
<span data-ttu-id="aa903-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="aa903-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa903-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="aa903-124">-Name</span></span>
<span data-ttu-id="aa903-125">資料流程名稱。</span><span class="sxs-lookup"><span data-stu-id="aa903-125">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: DataFlowName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa903-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa903-126">-ResourceGroupName</span></span>
<span data-ttu-id="aa903-127">資源組名。</span><span class="sxs-lookup"><span data-stu-id="aa903-127">The resource group name.</span></span>

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

### <span data-ttu-id="aa903-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa903-128">-ResourceId</span></span>
<span data-ttu-id="aa903-129">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="aa903-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="aa903-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa903-130">CommonParameters</span></span>
<span data-ttu-id="aa903-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="aa903-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa903-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aa903-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa903-133">輸入</span><span class="sxs-lookup"><span data-stu-id="aa903-133">INPUTS</span></span>

### <span data-ttu-id="aa903-134">System.String</span><span class="sxs-lookup"><span data-stu-id="aa903-134">System.String</span></span>

### <span data-ttu-id="aa903-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="aa903-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="aa903-136">輸出</span><span class="sxs-lookup"><span data-stu-id="aa903-136">OUTPUTS</span></span>

### <span data-ttu-id="aa903-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="aa903-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="aa903-138">筆記</span><span class="sxs-lookup"><span data-stu-id="aa903-138">NOTES</span></span>
<span data-ttu-id="aa903-139">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="aa903-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="aa903-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="aa903-140">RELATED LINKS</span></span>


