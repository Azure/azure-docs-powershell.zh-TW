---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
gitcommit: https://github.com/Azure/azure-powershell/blob/c396953644d237789e0f4e1f726b553913186d34
ms.openlocfilehash: bc60bbb5b48c4022e7db6a95e26a1f43ef891ae2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456739"
---
# <span data-ttu-id="2389d-101">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2389d-101">Get-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="2389d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2389d-102">SYNOPSIS</span></span>
<span data-ttu-id="2389d-103">取得資料工廠中觸發程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2389d-103">Gets information about triggers in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2389d-104">句法</span><span class="sxs-lookup"><span data-stu-id="2389d-104">SYNTAX</span></span>

### <span data-ttu-id="2389d-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="2389d-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### <span data-ttu-id="2389d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="2389d-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
```

## <span data-ttu-id="2389d-107">說明</span><span class="sxs-lookup"><span data-stu-id="2389d-107">DESCRIPTION</span></span>
<span data-ttu-id="2389d-108">AzureRmDataFactoryV2Trigger Cmdlet 會取得資料工廠中觸發 **程式** 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2389d-108">The **Get-AzureRmDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="2389d-109">如果您指定了觸發程式的名稱，此 Cmdlet 會取得該觸發程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2389d-109">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="2389d-110">如果您沒有指定名稱，此 Cmdlet 會取得資料工廠中所有觸發程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2389d-110">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>


## <span data-ttu-id="2389d-111">示例</span><span class="sxs-lookup"><span data-stu-id="2389d-111">EXAMPLES</span></span>

### <span data-ttu-id="2389d-112">範例1：取得特定觸發程式的相關資訊</span><span class="sxs-lookup"><span data-stu-id="2389d-112">Example 1: Get information about a specific trigger</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped

    TriggerName       : ScheduledTrigger2
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="2389d-113">取得在資料工廠 "WikiADF" 中所建立之所有觸發程式的清單。</span><span class="sxs-lookup"><span data-stu-id="2389d-113">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="2389d-114">範例2：取得所有觸發程式的相關資訊</span><span class="sxs-lookup"><span data-stu-id="2389d-114">Example 2: Get information about all triggers</span></span>

```
Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="2389d-115">取得資料工廠 "WikiADF" 中名為 "ScheduledTrigger" 的單一觸發程式。</span><span class="sxs-lookup"><span data-stu-id="2389d-115">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="2389d-116">參數</span><span class="sxs-lookup"><span data-stu-id="2389d-116">PARAMETERS</span></span>

### <span data-ttu-id="2389d-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="2389d-117">-DataFactory</span></span>
<span data-ttu-id="2389d-118">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="2389d-118">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2389d-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2389d-119">-DataFactoryName</span></span>
<span data-ttu-id="2389d-120">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="2389d-120">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2389d-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="2389d-121">-Name</span></span>
<span data-ttu-id="2389d-122">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="2389d-122">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2389d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2389d-123">-ResourceGroupName</span></span>
<span data-ttu-id="2389d-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2389d-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="2389d-125">輸入</span><span class="sxs-lookup"><span data-stu-id="2389d-125">INPUTS</span></span>

### <span data-ttu-id="2389d-126">System.object</span><span class="sxs-lookup"><span data-stu-id="2389d-126">System.String</span></span>
<span data-ttu-id="2389d-127">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="2389d-127">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="2389d-128">輸出</span><span class="sxs-lookup"><span data-stu-id="2389d-128">OUTPUTS</span></span>

### <span data-ttu-id="2389d-129">[System.object]。清單 ' 1 [DataFactoryV2. PSTrigger，DataFactoryV2，版本 = 0.1.9.0，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="2389d-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="2389d-130">PSTrigger 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="2389d-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="2389d-131">筆記</span><span class="sxs-lookup"><span data-stu-id="2389d-131">NOTES</span></span>

## <span data-ttu-id="2389d-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="2389d-132">RELATED LINKS</span></span>
[<span data-ttu-id="2389d-133">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2389d-133">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="2389d-134">開始-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2389d-134">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="2389d-135">停止 AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2389d-135">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="2389d-136">移除-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2389d-136">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
