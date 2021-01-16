---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: 5844863cf56008d5d73fae7eef644dfd8e27c239
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98282336"
---
# <span data-ttu-id="d65f0-101">Get-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="d65f0-101">Get-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="d65f0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d65f0-102">SYNOPSIS</span></span>
<span data-ttu-id="d65f0-103">傳回有關觸發程式執行的資訊。</span><span class="sxs-lookup"><span data-stu-id="d65f0-103">Returns information about trigger runs.</span></span>

## <span data-ttu-id="d65f0-104">句法</span><span class="sxs-lookup"><span data-stu-id="d65f0-104">SYNTAX</span></span>

### <span data-ttu-id="d65f0-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="d65f0-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d65f0-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d65f0-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d65f0-107">說明</span><span class="sxs-lookup"><span data-stu-id="d65f0-107">DESCRIPTION</span></span>
<span data-ttu-id="d65f0-108">[ **取得 AzDataFactoryV2TriggerRun** ] 命令會傳回指定的觸發程式在指定時間範圍內觸發程式執行的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="d65f0-108">The **Get-AzDataFactoryV2TriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="d65f0-109">示例</span><span class="sxs-lookup"><span data-stu-id="d65f0-109">EXAMPLES</span></span>

### <span data-ttu-id="d65f0-110">範例1：取得觸發程式執行的相關資訊</span><span class="sxs-lookup"><span data-stu-id="d65f0-110">Example 1: Get information about trigger run</span></span>
```
PS C:\> Get-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "WikiTrigger" -TriggerRunStartedAfter "2017-09-01" -TriggerRunStartedBefore "2019-09-30"

    ResourceGroupName   : ADF
    DataFactoryName     : WikiADF
    TriggerName         : WikiTrigger
    TriggerRunId        : 08586958400454144995526033731
    TriggerType         : ScheduleTrigger
    TriggerRunTimestamp : 9/18/2017 8:34:00 PM
    Status              : Succeeded
```

<span data-ttu-id="d65f0-111">這個命令會顯示在「2017-09-01」和「2019-09-30」之間開始「WikiADF」的「WikiTrigger」執行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d65f0-111">This command shows information about runs for "WikiTrigger" in the factory "WikiADF" that started between "2017-09-01" and "2019-09-30".</span></span>

## <span data-ttu-id="d65f0-112">參數</span><span class="sxs-lookup"><span data-stu-id="d65f0-112">PARAMETERS</span></span>

### <span data-ttu-id="d65f0-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d65f0-113">-DataFactory</span></span>
<span data-ttu-id="d65f0-114">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="d65f0-114">The data factory object.</span></span>

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

### <span data-ttu-id="d65f0-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d65f0-115">-DataFactoryName</span></span>
<span data-ttu-id="d65f0-116">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="d65f0-116">The data factory name.</span></span>

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

### <span data-ttu-id="d65f0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d65f0-117">-DefaultProfile</span></span>
<span data-ttu-id="d65f0-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d65f0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d65f0-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="d65f0-119">-Name</span></span>
<span data-ttu-id="d65f0-120">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="d65f0-120">The trigger name.</span></span>

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

### <span data-ttu-id="d65f0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d65f0-121">-ResourceGroupName</span></span>
<span data-ttu-id="d65f0-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d65f0-122">The resource group name.</span></span>

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

### <span data-ttu-id="d65f0-123">-TriggerRunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="d65f0-123">-TriggerRunStartedAfter</span></span>
<span data-ttu-id="d65f0-124">觸發程式執行開始之後或之後的時間，以 ISO8601 格式執行。</span><span class="sxs-lookup"><span data-stu-id="d65f0-124">The time at or after which the trigger run started to execute in ISO8601 format.</span></span>

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

### <span data-ttu-id="d65f0-125">-TriggerRunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="d65f0-125">-TriggerRunStartedBefore</span></span>
<span data-ttu-id="d65f0-126">觸發程式執行開始之前或之前的時間，以 ISO8601 格式執行。</span><span class="sxs-lookup"><span data-stu-id="d65f0-126">The time at or before which the trigger run started to execute in ISO8601 format.</span></span>

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

### <span data-ttu-id="d65f0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d65f0-127">CommonParameters</span></span>
<span data-ttu-id="d65f0-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d65f0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d65f0-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d65f0-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d65f0-130">輸入</span><span class="sxs-lookup"><span data-stu-id="d65f0-130">INPUTS</span></span>

### <span data-ttu-id="d65f0-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d65f0-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="d65f0-132">System.object</span><span class="sxs-lookup"><span data-stu-id="d65f0-132">System.String</span></span>

## <span data-ttu-id="d65f0-133">輸出</span><span class="sxs-lookup"><span data-stu-id="d65f0-133">OUTPUTS</span></span>

### <span data-ttu-id="d65f0-134">PSTriggerRun 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="d65f0-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

## <span data-ttu-id="d65f0-135">筆記</span><span class="sxs-lookup"><span data-stu-id="d65f0-135">NOTES</span></span>

## <span data-ttu-id="d65f0-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="d65f0-136">RELATED LINKS</span></span>

[<span data-ttu-id="d65f0-137">開始-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="d65f0-137">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="d65f0-138">停止 AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="d65f0-138">Stop-AzDataFactoryV2Trigger</span></span>]()

