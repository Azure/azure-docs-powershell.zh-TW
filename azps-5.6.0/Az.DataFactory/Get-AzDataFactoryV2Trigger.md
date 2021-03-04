---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 5940d362b3c06ede714568daa2ecce8bd829581d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907705"
---
# <span data-ttu-id="98f00-101">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="98f00-101">Get-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="98f00-102">簡介</span><span class="sxs-lookup"><span data-stu-id="98f00-102">SYNOPSIS</span></span>
<span data-ttu-id="98f00-103">在資料工廠中，獲得觸發者相關資訊。</span><span class="sxs-lookup"><span data-stu-id="98f00-103">Gets information about triggers in a data factory.</span></span>

## <span data-ttu-id="98f00-104">語法</span><span class="sxs-lookup"><span data-stu-id="98f00-104">SYNTAX</span></span>

### <span data-ttu-id="98f00-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="98f00-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98f00-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="98f00-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98f00-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="98f00-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Trigger [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="98f00-108">描述</span><span class="sxs-lookup"><span data-stu-id="98f00-108">DESCRIPTION</span></span>
<span data-ttu-id="98f00-109">**Get-AzDataFactoryV2Trigger Cmdlet** 會取得資料工廠中觸發程式的資訊。</span><span class="sxs-lookup"><span data-stu-id="98f00-109">The **Get-AzDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="98f00-110">如果您指定觸發者的名稱，Cmdlet 會獲得該觸發人的資訊。</span><span class="sxs-lookup"><span data-stu-id="98f00-110">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="98f00-111">如果您未指定名稱，Cmdlet 會獲得資料工廠中所有觸發者的資訊。</span><span class="sxs-lookup"><span data-stu-id="98f00-111">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>

## <span data-ttu-id="98f00-112">例子</span><span class="sxs-lookup"><span data-stu-id="98f00-112">EXAMPLES</span></span>

### <span data-ttu-id="98f00-113">範例 1：取得所有觸發人的資訊</span><span class="sxs-lookup"><span data-stu-id="98f00-113">Example 1: Get information about all triggers</span></span>
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

<span data-ttu-id="98f00-114">在資料工廠 「WikiADF」中建立的所有觸發者清單。</span><span class="sxs-lookup"><span data-stu-id="98f00-114">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="98f00-115">範例 2：取得特定觸發者的資訊</span><span class="sxs-lookup"><span data-stu-id="98f00-115">Example 2: Get information about a specific trigger</span></span>
```
Get-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="98f00-116">在資料工廠 「WikiADF」中，獲得一個稱為「ScheduledTri用」的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="98f00-116">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="98f00-117">參數</span><span class="sxs-lookup"><span data-stu-id="98f00-117">PARAMETERS</span></span>

### <span data-ttu-id="98f00-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="98f00-118">-DataFactory</span></span>
<span data-ttu-id="98f00-119">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="98f00-119">The data factory object.</span></span>

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

### <span data-ttu-id="98f00-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="98f00-120">-DataFactoryName</span></span>
<span data-ttu-id="98f00-121">資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="98f00-121">The data factory name.</span></span>

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

### <span data-ttu-id="98f00-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98f00-122">-DefaultProfile</span></span>
<span data-ttu-id="98f00-123">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="98f00-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98f00-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="98f00-124">-Name</span></span>
<span data-ttu-id="98f00-125">觸發者名稱。</span><span class="sxs-lookup"><span data-stu-id="98f00-125">The trigger name.</span></span>

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

### <span data-ttu-id="98f00-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98f00-126">-ResourceGroupName</span></span>
<span data-ttu-id="98f00-127">資源組名。</span><span class="sxs-lookup"><span data-stu-id="98f00-127">The resource group name.</span></span>

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

### <span data-ttu-id="98f00-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98f00-128">-ResourceId</span></span>
<span data-ttu-id="98f00-129">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="98f00-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="98f00-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98f00-130">CommonParameters</span></span>
<span data-ttu-id="98f00-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="98f00-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98f00-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="98f00-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98f00-133">輸入</span><span class="sxs-lookup"><span data-stu-id="98f00-133">INPUTS</span></span>

### <span data-ttu-id="98f00-134">System.String</span><span class="sxs-lookup"><span data-stu-id="98f00-134">System.String</span></span>

### <span data-ttu-id="98f00-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="98f00-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="98f00-136">輸出</span><span class="sxs-lookup"><span data-stu-id="98f00-136">OUTPUTS</span></span>

### <span data-ttu-id="98f00-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="98f00-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="98f00-138">筆記</span><span class="sxs-lookup"><span data-stu-id="98f00-138">NOTES</span></span>

## <span data-ttu-id="98f00-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="98f00-139">RELATED LINKS</span></span>

[<span data-ttu-id="98f00-140">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="98f00-140">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="98f00-141">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="98f00-141">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="98f00-142">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="98f00-142">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="98f00-143">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="98f00-143">Remove-AzDataFactoryV2Trigger</span></span>]()
