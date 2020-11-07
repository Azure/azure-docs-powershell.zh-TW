---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
ms.openlocfilehash: 7d3f1ca73712753ad38b46c186a51bd7aa159b46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623718"
---
# <span data-ttu-id="8e061-101">Get-AzureRmDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="8e061-101">Get-AzureRmDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="8e061-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8e061-102">SYNOPSIS</span></span>
<span data-ttu-id="8e061-103">傳回有關觸發程式執行的資訊。</span><span class="sxs-lookup"><span data-stu-id="8e061-103">Returns information about trigger runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e061-104">句法</span><span class="sxs-lookup"><span data-stu-id="8e061-104">SYNTAX</span></span>

### <span data-ttu-id="8e061-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="8e061-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e061-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8e061-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e061-107">說明</span><span class="sxs-lookup"><span data-stu-id="8e061-107">DESCRIPTION</span></span>
<span data-ttu-id="8e061-108">[ **取得 AzureRmDataFactoryV2TriggerRun** ] 命令會傳回指定的觸發程式在指定時間範圍內觸發程式執行的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="8e061-108">The **Get-AzureRmDataFactoryV2TriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="8e061-109">示例</span><span class="sxs-lookup"><span data-stu-id="8e061-109">EXAMPLES</span></span>

### <span data-ttu-id="8e061-110">範例1：取得觸發程式執行的相關資訊</span><span class="sxs-lookup"><span data-stu-id="8e061-110">Example 1: Get information about trigger run</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "WikiTrigger" -TriggerRunStartedAfter "2017-09-01" -TriggerRunStartedBefore "2019-09-30"

    ResourceGroupName   : ADF
    DataFactoryName     : WikiADF
    TriggerName         : WikiTrigger
    TriggerRunId        : 08586958400454144995526033731
    TriggerType         : ScheduleTrigger
    TriggerRunTimestamp : 9/18/2017 8:34:00 PM
    Status              : Succeeded
```

<span data-ttu-id="8e061-111">這個命令會顯示在「2017-09-01」和「2019-09-30」之間開始「WikiADF」的「WikiTrigger」執行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8e061-111">This command shows information about runs for "WikiTrigger" in the factory "WikiADF" that started between "2017-09-01" and "2019-09-30".</span></span>

## <span data-ttu-id="8e061-112">參數</span><span class="sxs-lookup"><span data-stu-id="8e061-112">PARAMETERS</span></span>

### <span data-ttu-id="8e061-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="8e061-113">-DataFactory</span></span>
<span data-ttu-id="8e061-114">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="8e061-114">The data factory object.</span></span>

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

### <span data-ttu-id="8e061-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8e061-115">-DataFactoryName</span></span>
<span data-ttu-id="8e061-116">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="8e061-116">The data factory name.</span></span>

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

### <span data-ttu-id="8e061-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="8e061-117">-Name</span></span>
<span data-ttu-id="8e061-118">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="8e061-118">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e061-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e061-119">-ResourceGroupName</span></span>
<span data-ttu-id="8e061-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e061-120">The resource group name.</span></span>

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

### <span data-ttu-id="8e061-121">-TriggerRunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="8e061-121">-TriggerRunStartedAfter</span></span>
<span data-ttu-id="8e061-122">觸發程式執行開始之後或之後的時間，以 ISO8601 格式執行。</span><span class="sxs-lookup"><span data-stu-id="8e061-122">The time at or after which the trigger run started to execute in ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e061-123">-TriggerRunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="8e061-123">-TriggerRunStartedBefore</span></span>
<span data-ttu-id="8e061-124">觸發程式執行開始之前或之前的時間，以 ISO8601 格式執行。</span><span class="sxs-lookup"><span data-stu-id="8e061-124">The time at or before which the trigger run started to execute in ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e061-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e061-125">-DefaultProfile</span></span>
<span data-ttu-id="8e061-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8e061-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e061-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e061-127">CommonParameters</span></span>
<span data-ttu-id="8e061-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8e061-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e061-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8e061-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e061-130">輸入</span><span class="sxs-lookup"><span data-stu-id="8e061-130">INPUTS</span></span>

### <span data-ttu-id="8e061-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="8e061-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="8e061-132">System.object</span><span class="sxs-lookup"><span data-stu-id="8e061-132">System.String</span></span>

## <span data-ttu-id="8e061-133">輸出</span><span class="sxs-lookup"><span data-stu-id="8e061-133">OUTPUTS</span></span>

### <span data-ttu-id="8e061-134">[System.object]。清單 ' 1 [DataFactoryV2. PSTriggerRun，DataFactoryV2，版本 = 0.1.9.0，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="8e061-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="8e061-135">PSTriggerRun 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="8e061-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

## <span data-ttu-id="8e061-136">筆記</span><span class="sxs-lookup"><span data-stu-id="8e061-136">NOTES</span></span>

## <span data-ttu-id="8e061-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="8e061-137">RELATED LINKS</span></span>

[<span data-ttu-id="8e061-138">開始-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="8e061-138">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="8e061-139">停止 AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="8e061-139">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

