---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 7c14b5c53cdffa51671a64ad40fe18a400ae6803
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453808"
---
# <span data-ttu-id="88238-101">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="88238-101">Get-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="88238-102">摘要</span><span class="sxs-lookup"><span data-stu-id="88238-102">SYNOPSIS</span></span>
<span data-ttu-id="88238-103">取得資料工廠中觸發程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="88238-103">Gets information about triggers in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88238-104">句法</span><span class="sxs-lookup"><span data-stu-id="88238-104">SYNTAX</span></span>

### <span data-ttu-id="88238-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="88238-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88238-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="88238-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88238-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="88238-107">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="88238-108">說明</span><span class="sxs-lookup"><span data-stu-id="88238-108">DESCRIPTION</span></span>
<span data-ttu-id="88238-109">AzureRmDataFactoryV2Trigger Cmdlet 會取得資料工廠中觸發 **程式** 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="88238-109">The **Get-AzureRmDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="88238-110">如果您指定了觸發程式的名稱，此 Cmdlet 會取得該觸發程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="88238-110">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="88238-111">如果您沒有指定名稱，此 Cmdlet 會取得資料工廠中所有觸發程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="88238-111">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>

## <span data-ttu-id="88238-112">示例</span><span class="sxs-lookup"><span data-stu-id="88238-112">EXAMPLES</span></span>

### <span data-ttu-id="88238-113">範例1：取得特定觸發程式的相關資訊</span><span class="sxs-lookup"><span data-stu-id="88238-113">Example 1: Get information about a specific trigger</span></span>
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

<span data-ttu-id="88238-114">取得在資料工廠 "WikiADF" 中所建立之所有觸發程式的清單。</span><span class="sxs-lookup"><span data-stu-id="88238-114">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="88238-115">範例2：取得所有觸發程式的相關資訊</span><span class="sxs-lookup"><span data-stu-id="88238-115">Example 2: Get information about all triggers</span></span>
```
Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="88238-116">取得資料工廠 "WikiADF" 中名為 "ScheduledTrigger" 的單一觸發程式。</span><span class="sxs-lookup"><span data-stu-id="88238-116">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="88238-117">參數</span><span class="sxs-lookup"><span data-stu-id="88238-117">PARAMETERS</span></span>

### <span data-ttu-id="88238-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="88238-118">-DataFactory</span></span>
<span data-ttu-id="88238-119">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="88238-119">The data factory object.</span></span>

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

### <span data-ttu-id="88238-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="88238-120">-DataFactoryName</span></span>
<span data-ttu-id="88238-121">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="88238-121">The data factory name.</span></span>

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

### <span data-ttu-id="88238-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88238-122">-DefaultProfile</span></span>
<span data-ttu-id="88238-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="88238-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88238-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="88238-124">-Name</span></span>
<span data-ttu-id="88238-125">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="88238-125">The trigger name.</span></span>

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

### <span data-ttu-id="88238-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88238-126">-ResourceGroupName</span></span>
<span data-ttu-id="88238-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="88238-127">The resource group name.</span></span>

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

### <span data-ttu-id="88238-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88238-128">-ResourceId</span></span>
<span data-ttu-id="88238-129">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="88238-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="88238-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88238-130">CommonParameters</span></span>
<span data-ttu-id="88238-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="88238-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88238-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="88238-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88238-133">輸入</span><span class="sxs-lookup"><span data-stu-id="88238-133">INPUTS</span></span>

### <span data-ttu-id="88238-134">System.object</span><span class="sxs-lookup"><span data-stu-id="88238-134">System.String</span></span>

### <span data-ttu-id="88238-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="88238-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="88238-136">參數： DataFactory (ByValue) </span><span class="sxs-lookup"><span data-stu-id="88238-136">Parameters: DataFactory (ByValue)</span></span>

## <span data-ttu-id="88238-137">輸出</span><span class="sxs-lookup"><span data-stu-id="88238-137">OUTPUTS</span></span>

### <span data-ttu-id="88238-138">PSTrigger 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="88238-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="88238-139">筆記</span><span class="sxs-lookup"><span data-stu-id="88238-139">NOTES</span></span>

## <span data-ttu-id="88238-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="88238-140">RELATED LINKS</span></span>

[<span data-ttu-id="88238-141">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="88238-141">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="88238-142">開始-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="88238-142">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="88238-143">停止 AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="88238-143">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="88238-144">移除-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="88238-144">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
