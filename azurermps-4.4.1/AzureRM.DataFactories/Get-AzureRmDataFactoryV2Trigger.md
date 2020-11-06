---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 3d5db6b7aa1b7c2ffdd63292696230e2d12bd4c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447131"
---
# <span data-ttu-id="cb1c0-101">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="cb1c0-101">Get-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="cb1c0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cb1c0-102">SYNOPSIS</span></span>
<span data-ttu-id="cb1c0-103">取得資料工廠中觸發程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cb1c0-103">Gets information about triggers in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb1c0-104">句法</span><span class="sxs-lookup"><span data-stu-id="cb1c0-104">SYNTAX</span></span>

### <span data-ttu-id="cb1c0-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="cb1c0-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb1c0-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="cb1c0-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb1c0-107">說明</span><span class="sxs-lookup"><span data-stu-id="cb1c0-107">DESCRIPTION</span></span>
<span data-ttu-id="cb1c0-108">AzureRmDataFactoryV2Trigger Cmdlet 會取得資料工廠中觸發 **程式** 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cb1c0-108">The **Get-AzureRmDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="cb1c0-109">如果您指定了觸發程式的名稱，此 Cmdlet 會取得該觸發程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cb1c0-109">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="cb1c0-110">如果您沒有指定名稱，此 Cmdlet 會取得資料工廠中所有觸發程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cb1c0-110">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>

## <span data-ttu-id="cb1c0-111">示例</span><span class="sxs-lookup"><span data-stu-id="cb1c0-111">EXAMPLES</span></span>

### <span data-ttu-id="cb1c0-112">範例1：取得特定觸發程式的相關資訊</span><span class="sxs-lookup"><span data-stu-id="cb1c0-112">Example 1: Get information about a specific trigger</span></span>
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

<span data-ttu-id="cb1c0-113">取得在資料工廠 "WikiADF" 中所建立之所有觸發程式的清單。</span><span class="sxs-lookup"><span data-stu-id="cb1c0-113">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="cb1c0-114">範例2：取得所有觸發程式的相關資訊</span><span class="sxs-lookup"><span data-stu-id="cb1c0-114">Example 2: Get information about all triggers</span></span>
```
Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="cb1c0-115">取得資料工廠 "WikiADF" 中名為 "ScheduledTrigger" 的單一觸發程式。</span><span class="sxs-lookup"><span data-stu-id="cb1c0-115">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="cb1c0-116">參數</span><span class="sxs-lookup"><span data-stu-id="cb1c0-116">PARAMETERS</span></span>

### <span data-ttu-id="cb1c0-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb1c0-117">-DataFactory</span></span>
<span data-ttu-id="cb1c0-118">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="cb1c0-118">The data factory object.</span></span>

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

### <span data-ttu-id="cb1c0-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="cb1c0-119">-DataFactoryName</span></span>
<span data-ttu-id="cb1c0-120">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="cb1c0-120">The data factory name.</span></span>

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

### <span data-ttu-id="cb1c0-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="cb1c0-121">-Name</span></span>
<span data-ttu-id="cb1c0-122">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="cb1c0-122">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb1c0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb1c0-123">-ResourceGroupName</span></span>
<span data-ttu-id="cb1c0-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb1c0-124">The resource group name.</span></span>

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

### <span data-ttu-id="cb1c0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb1c0-125">-DefaultProfile</span></span>
<span data-ttu-id="cb1c0-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cb1c0-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb1c0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb1c0-127">CommonParameters</span></span>
<span data-ttu-id="cb1c0-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cb1c0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb1c0-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cb1c0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb1c0-130">輸入</span><span class="sxs-lookup"><span data-stu-id="cb1c0-130">INPUTS</span></span>

### <span data-ttu-id="cb1c0-131">System.object</span><span class="sxs-lookup"><span data-stu-id="cb1c0-131">System.String</span></span>
<span data-ttu-id="cb1c0-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="cb1c0-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="cb1c0-133">輸出</span><span class="sxs-lookup"><span data-stu-id="cb1c0-133">OUTPUTS</span></span>

### <span data-ttu-id="cb1c0-134">[System.object]。清單 ' 1 [DataFactoryV2. PSTrigger，DataFactoryV2，版本 = 0.1.9.0，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="cb1c0-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="cb1c0-135">PSTrigger 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="cb1c0-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="cb1c0-136">筆記</span><span class="sxs-lookup"><span data-stu-id="cb1c0-136">NOTES</span></span>

## <span data-ttu-id="cb1c0-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="cb1c0-137">RELATED LINKS</span></span>

[<span data-ttu-id="cb1c0-138">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="cb1c0-138">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="cb1c0-139">開始-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="cb1c0-139">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="cb1c0-140">停止 AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="cb1c0-140">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="cb1c0-141">移除-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="cb1c0-141">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
