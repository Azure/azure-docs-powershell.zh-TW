---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: b4af5eae61e47d8617eb270451f406f349162f50
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971160"
---
# <span data-ttu-id="71bd4-101">Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="71bd4-101">Get-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="71bd4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="71bd4-102">SYNOPSIS</span></span>
<span data-ttu-id="71bd4-103">取得資料工廠中資料流程的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="71bd4-103">Gets information about data flows in Data Factory.</span></span>

## <span data-ttu-id="71bd4-104">句法</span><span class="sxs-lookup"><span data-stu-id="71bd4-104">SYNTAX</span></span>

### <span data-ttu-id="71bd4-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="71bd4-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71bd4-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="71bd4-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71bd4-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="71bd4-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlow [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="71bd4-108">說明</span><span class="sxs-lookup"><span data-stu-id="71bd4-108">DESCRIPTION</span></span>
<span data-ttu-id="71bd4-109">Get-AzDataFactoryV2DataFlow Cmdlet 會取得 Azure 資料工廠中資料流程的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="71bd4-109">The Get-AzDataFactoryV2DataFlow cmdlet gets information about data flows in Azure Data Factory.</span></span>
<span data-ttu-id="71bd4-110">如果您指定資料流程程的名稱，此 Cmdlet 會取得該資料流程的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="71bd4-110">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="71bd4-111">如果您沒有指定名稱，此 Cmdlet 會取得資料工廠中所有資料流程的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="71bd4-111">If you do not specify a name, this cmdlet gets information about all the data flows in the data factory.</span></span>

## <span data-ttu-id="71bd4-112">示例</span><span class="sxs-lookup"><span data-stu-id="71bd4-112">EXAMPLES</span></span>
### <span data-ttu-id="71bd4-113">範例1：取得所有資料流程程的相關資訊</span><span class="sxs-lookup"><span data-stu-id="71bd4-113">Example 1: Get information about all data flows</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow3                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="71bd4-114">這個命令會取得資料工廠（名為 WikiADF）中所有資料流程的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="71bd4-114">This command gets information about all data flows in the data factory named WikiADF.</span></span>

### <span data-ttu-id="71bd4-115">範例2：取得特定資料流程程的相關資訊</span><span class="sxs-lookup"><span data-stu-id="71bd4-115">Example 2: Get information about a specific data flow</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "dataflow1"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="71bd4-116">這個命令會取得資料工廠（名為 WikiADF）中名為 dataflow1 的資料流程的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="71bd4-116">This command gets information about the data flow named dataflow1 in the data factory named WikiADF.</span></span>

## <span data-ttu-id="71bd4-117">參數</span><span class="sxs-lookup"><span data-stu-id="71bd4-117">PARAMETERS</span></span>

### <span data-ttu-id="71bd4-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="71bd4-118">-DataFactory</span></span>
<span data-ttu-id="71bd4-119">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="71bd4-119">The data factory object.</span></span>

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

### <span data-ttu-id="71bd4-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="71bd4-120">-DataFactoryName</span></span>
<span data-ttu-id="71bd4-121">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="71bd4-121">The data factory name.</span></span>

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

### <span data-ttu-id="71bd4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71bd4-122">-DefaultProfile</span></span>
<span data-ttu-id="71bd4-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="71bd4-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71bd4-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="71bd4-124">-Name</span></span>
<span data-ttu-id="71bd4-125">資料流程程名稱。</span><span class="sxs-lookup"><span data-stu-id="71bd4-125">The data flow name.</span></span>

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

### <span data-ttu-id="71bd4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71bd4-126">-ResourceGroupName</span></span>
<span data-ttu-id="71bd4-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="71bd4-127">The resource group name.</span></span>

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

### <span data-ttu-id="71bd4-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71bd4-128">-ResourceId</span></span>
<span data-ttu-id="71bd4-129">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="71bd4-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="71bd4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71bd4-130">CommonParameters</span></span>
<span data-ttu-id="71bd4-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="71bd4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71bd4-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="71bd4-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71bd4-133">輸入</span><span class="sxs-lookup"><span data-stu-id="71bd4-133">INPUTS</span></span>

### <span data-ttu-id="71bd4-134">System.object</span><span class="sxs-lookup"><span data-stu-id="71bd4-134">System.String</span></span>

### <span data-ttu-id="71bd4-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="71bd4-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="71bd4-136">輸出</span><span class="sxs-lookup"><span data-stu-id="71bd4-136">OUTPUTS</span></span>

### <span data-ttu-id="71bd4-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="71bd4-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="71bd4-138">筆記</span><span class="sxs-lookup"><span data-stu-id="71bd4-138">NOTES</span></span>
<span data-ttu-id="71bd4-139">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="71bd4-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="71bd4-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="71bd4-140">RELATED LINKS</span></span>

[<span data-ttu-id="71bd4-141">Set-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="71bd4-141">Set-AzDataFactoryDataFlow</span></span>](./Set-AzDataFactoryDataFlow.md)

[<span data-ttu-id="71bd4-142">移除-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="71bd4-142">Remove-AzDataFactoryDataFlow</span></span>](./Remove-AzDataFactoryDataFlow.md)