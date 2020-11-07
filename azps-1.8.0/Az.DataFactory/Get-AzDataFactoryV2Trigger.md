---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
ms.openlocfilehash: e5afbdd389d1ee9e1b74895743ed47ceed0b4ae9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788170"
---
# <span data-ttu-id="79364-101">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="79364-101">Get-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="79364-102">摘要</span><span class="sxs-lookup"><span data-stu-id="79364-102">SYNOPSIS</span></span>
<span data-ttu-id="79364-103">取得資料工廠中觸發程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="79364-103">Gets information about triggers in a data factory.</span></span>

## <span data-ttu-id="79364-104">句法</span><span class="sxs-lookup"><span data-stu-id="79364-104">SYNTAX</span></span>

### <span data-ttu-id="79364-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="79364-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79364-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="79364-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79364-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="79364-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Trigger [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="79364-108">說明</span><span class="sxs-lookup"><span data-stu-id="79364-108">DESCRIPTION</span></span>
<span data-ttu-id="79364-109">AzDataFactoryV2Trigger Cmdlet 會取得資料工廠中觸發 **程式** 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="79364-109">The **Get-AzDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="79364-110">如果您指定了觸發程式的名稱，此 Cmdlet 會取得該觸發程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="79364-110">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="79364-111">如果您沒有指定名稱，此 Cmdlet 會取得資料工廠中所有觸發程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="79364-111">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>

## <span data-ttu-id="79364-112">示例</span><span class="sxs-lookup"><span data-stu-id="79364-112">EXAMPLES</span></span>

### <span data-ttu-id="79364-113">範例1：取得特定觸發程式的相關資訊</span><span class="sxs-lookup"><span data-stu-id="79364-113">Example 1: Get information about a specific trigger</span></span>
```
PS C:\> Get-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

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

<span data-ttu-id="79364-114">取得在資料工廠 "WikiADF" 中所建立之所有觸發程式的清單。</span><span class="sxs-lookup"><span data-stu-id="79364-114">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="79364-115">範例2：取得所有觸發程式的相關資訊</span><span class="sxs-lookup"><span data-stu-id="79364-115">Example 2: Get information about all triggers</span></span>
```
Get-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="79364-116">取得資料工廠 "WikiADF" 中名為 "ScheduledTrigger" 的單一觸發程式。</span><span class="sxs-lookup"><span data-stu-id="79364-116">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="79364-117">參數</span><span class="sxs-lookup"><span data-stu-id="79364-117">PARAMETERS</span></span>

### <span data-ttu-id="79364-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="79364-118">-DataFactory</span></span>
<span data-ttu-id="79364-119">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="79364-119">The data factory object.</span></span>

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

### <span data-ttu-id="79364-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="79364-120">-DataFactoryName</span></span>
<span data-ttu-id="79364-121">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="79364-121">The data factory name.</span></span>

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

### <span data-ttu-id="79364-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79364-122">-DefaultProfile</span></span>
<span data-ttu-id="79364-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="79364-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79364-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="79364-124">-Name</span></span>
<span data-ttu-id="79364-125">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="79364-125">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79364-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79364-126">-ResourceGroupName</span></span>
<span data-ttu-id="79364-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="79364-127">The resource group name.</span></span>

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

### <span data-ttu-id="79364-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79364-128">-ResourceId</span></span>
<span data-ttu-id="79364-129">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="79364-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="79364-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79364-130">CommonParameters</span></span>
<span data-ttu-id="79364-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="79364-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79364-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="79364-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79364-133">輸入</span><span class="sxs-lookup"><span data-stu-id="79364-133">INPUTS</span></span>

### <span data-ttu-id="79364-134">System.object</span><span class="sxs-lookup"><span data-stu-id="79364-134">System.String</span></span>

### <span data-ttu-id="79364-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="79364-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="79364-136">輸出</span><span class="sxs-lookup"><span data-stu-id="79364-136">OUTPUTS</span></span>

### <span data-ttu-id="79364-137">PSTrigger 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="79364-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="79364-138">筆記</span><span class="sxs-lookup"><span data-stu-id="79364-138">NOTES</span></span>

## <span data-ttu-id="79364-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="79364-139">RELATED LINKS</span></span>

[<span data-ttu-id="79364-140">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="79364-140">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="79364-141">開始-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="79364-141">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="79364-142">停止 AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="79364-142">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="79364-143">移除-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="79364-143">Remove-AzDataFactoryV2Trigger</span></span>]()
