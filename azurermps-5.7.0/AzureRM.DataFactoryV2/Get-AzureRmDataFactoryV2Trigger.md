---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 5004b50cf5bb5b22a95ef00bf19f0e783fd04cb2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455448"
---
# <span data-ttu-id="2bab2-101">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2bab2-101">Get-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="2bab2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2bab2-102">SYNOPSIS</span></span>
<span data-ttu-id="2bab2-103">取得資料工廠中觸發程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2bab2-103">Gets information about triggers in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bab2-104">句法</span><span class="sxs-lookup"><span data-stu-id="2bab2-104">SYNTAX</span></span>

### <span data-ttu-id="2bab2-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="2bab2-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2bab2-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="2bab2-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2bab2-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2bab2-107">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2Trigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2bab2-108">說明</span><span class="sxs-lookup"><span data-stu-id="2bab2-108">DESCRIPTION</span></span>
<span data-ttu-id="2bab2-109">AzureRmDataFactoryV2Trigger Cmdlet 會取得資料工廠中觸發 **程式** 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2bab2-109">The **Get-AzureRmDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="2bab2-110">如果您指定了觸發程式的名稱，此 Cmdlet 會取得該觸發程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2bab2-110">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="2bab2-111">如果您沒有指定名稱，此 Cmdlet 會取得資料工廠中所有觸發程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2bab2-111">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>

## <span data-ttu-id="2bab2-112">示例</span><span class="sxs-lookup"><span data-stu-id="2bab2-112">EXAMPLES</span></span>

### <span data-ttu-id="2bab2-113">範例1：取得特定觸發程式的相關資訊</span><span class="sxs-lookup"><span data-stu-id="2bab2-113">Example 1: Get information about a specific trigger</span></span>
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

<span data-ttu-id="2bab2-114">取得在資料工廠 "WikiADF" 中所建立之所有觸發程式的清單。</span><span class="sxs-lookup"><span data-stu-id="2bab2-114">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="2bab2-115">範例2：取得所有觸發程式的相關資訊</span><span class="sxs-lookup"><span data-stu-id="2bab2-115">Example 2: Get information about all triggers</span></span>
```
Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="2bab2-116">取得資料工廠 "WikiADF" 中名為 "ScheduledTrigger" 的單一觸發程式。</span><span class="sxs-lookup"><span data-stu-id="2bab2-116">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="2bab2-117">參數</span><span class="sxs-lookup"><span data-stu-id="2bab2-117">PARAMETERS</span></span>

### <span data-ttu-id="2bab2-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="2bab2-118">-DataFactory</span></span>
<span data-ttu-id="2bab2-119">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="2bab2-119">The data factory object.</span></span>

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

### <span data-ttu-id="2bab2-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2bab2-120">-DataFactoryName</span></span>
<span data-ttu-id="2bab2-121">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="2bab2-121">The data factory name.</span></span>

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

### <span data-ttu-id="2bab2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bab2-122">-DefaultProfile</span></span>
<span data-ttu-id="2bab2-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2bab2-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bab2-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="2bab2-124">-Name</span></span>
<span data-ttu-id="2bab2-125">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="2bab2-125">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bab2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bab2-126">-ResourceGroupName</span></span>
<span data-ttu-id="2bab2-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2bab2-127">The resource group name.</span></span>

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

### <span data-ttu-id="2bab2-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2bab2-128">-ResourceId</span></span>
<span data-ttu-id="2bab2-129">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2bab2-129">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bab2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bab2-130">CommonParameters</span></span>
<span data-ttu-id="2bab2-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2bab2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bab2-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2bab2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bab2-133">輸入</span><span class="sxs-lookup"><span data-stu-id="2bab2-133">INPUTS</span></span>

### <span data-ttu-id="2bab2-134">System.object</span><span class="sxs-lookup"><span data-stu-id="2bab2-134">System.String</span></span>
<span data-ttu-id="2bab2-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="2bab2-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="2bab2-136">輸出</span><span class="sxs-lookup"><span data-stu-id="2bab2-136">OUTPUTS</span></span>

### <span data-ttu-id="2bab2-137">[System.object]。清單 ' 1 [DataFactoryV2. PSTrigger，DataFactoryV2，版本 = 0.1.9.0，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="2bab2-137">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="2bab2-138">PSTrigger 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="2bab2-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="2bab2-139">筆記</span><span class="sxs-lookup"><span data-stu-id="2bab2-139">NOTES</span></span>

## <span data-ttu-id="2bab2-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="2bab2-140">RELATED LINKS</span></span>

[<span data-ttu-id="2bab2-141">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2bab2-141">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="2bab2-142">開始-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2bab2-142">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="2bab2-143">停止 AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2bab2-143">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="2bab2-144">移除-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2bab2-144">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
