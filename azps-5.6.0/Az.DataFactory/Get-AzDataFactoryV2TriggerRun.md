---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: ba9ea38f5915f5a89326c806e11a055ec6aeed75
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907702"
---
# <span data-ttu-id="fd963-101">Get-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="fd963-101">Get-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="fd963-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fd963-102">SYNOPSIS</span></span>
<span data-ttu-id="fd963-103">會返回觸發程式執行的資訊。</span><span class="sxs-lookup"><span data-stu-id="fd963-103">Returns information about trigger runs.</span></span>

## <span data-ttu-id="fd963-104">語法</span><span class="sxs-lookup"><span data-stu-id="fd963-104">SYNTAX</span></span>

### <span data-ttu-id="fd963-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="fd963-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd963-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="fd963-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd963-107">描述</span><span class="sxs-lookup"><span data-stu-id="fd963-107">DESCRIPTION</span></span>
<span data-ttu-id="fd963-108">**Get-AzDataFactoryV2TriggerRun** 命令會針對指定時間範圍內指定的觸發程式，會傳送觸發程式執行的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="fd963-108">The **Get-AzDataFactoryV2TriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="fd963-109">例子</span><span class="sxs-lookup"><span data-stu-id="fd963-109">EXAMPLES</span></span>

### <span data-ttu-id="fd963-110">範例 1：取得觸發程式執行的資訊</span><span class="sxs-lookup"><span data-stu-id="fd963-110">Example 1: Get information about trigger run</span></span>
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

<span data-ttu-id="fd963-111">此命令會顯示在 "2017-09-01" 和 "2019-09-30" 之間開始的「WikiTri用」工廠 「WikiTri用」執行資訊。</span><span class="sxs-lookup"><span data-stu-id="fd963-111">This command shows information about runs for "WikiTrigger" in the factory "WikiADF" that started between "2017-09-01" and "2019-09-30".</span></span>

## <span data-ttu-id="fd963-112">參數</span><span class="sxs-lookup"><span data-stu-id="fd963-112">PARAMETERS</span></span>

### <span data-ttu-id="fd963-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="fd963-113">-DataFactory</span></span>
<span data-ttu-id="fd963-114">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="fd963-114">The data factory object.</span></span>

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

### <span data-ttu-id="fd963-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="fd963-115">-DataFactoryName</span></span>
<span data-ttu-id="fd963-116">資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="fd963-116">The data factory name.</span></span>

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

### <span data-ttu-id="fd963-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd963-117">-DefaultProfile</span></span>
<span data-ttu-id="fd963-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fd963-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd963-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="fd963-119">-Name</span></span>
<span data-ttu-id="fd963-120">觸發者名稱。</span><span class="sxs-lookup"><span data-stu-id="fd963-120">The trigger name.</span></span>

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

### <span data-ttu-id="fd963-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd963-121">-ResourceGroupName</span></span>
<span data-ttu-id="fd963-122">資源組名。</span><span class="sxs-lookup"><span data-stu-id="fd963-122">The resource group name.</span></span>

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

### <span data-ttu-id="fd963-123">-TriggerRunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="fd963-123">-TriggerRunStartedAfter</span></span>
<span data-ttu-id="fd963-124">觸發程式執行開始以 ISO8601 格式執行的時間。</span><span class="sxs-lookup"><span data-stu-id="fd963-124">The time at or after which the trigger run started to execute in ISO8601 format.</span></span>

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

### <span data-ttu-id="fd963-125">-TriggerRunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="fd963-125">-TriggerRunStartedBefore</span></span>
<span data-ttu-id="fd963-126">觸發程式執行開始以 ISO8601 格式執行的時間。</span><span class="sxs-lookup"><span data-stu-id="fd963-126">The time at or before which the trigger run started to execute in ISO8601 format.</span></span>

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

### <span data-ttu-id="fd963-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd963-127">CommonParameters</span></span>
<span data-ttu-id="fd963-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fd963-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd963-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="fd963-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd963-130">輸入</span><span class="sxs-lookup"><span data-stu-id="fd963-130">INPUTS</span></span>

### <span data-ttu-id="fd963-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="fd963-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="fd963-132">System.String</span><span class="sxs-lookup"><span data-stu-id="fd963-132">System.String</span></span>

## <span data-ttu-id="fd963-133">輸出</span><span class="sxs-lookup"><span data-stu-id="fd963-133">OUTPUTS</span></span>

### <span data-ttu-id="fd963-134">Microsoft.Azure.Commands.DataFactoryV2.models.PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="fd963-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

## <span data-ttu-id="fd963-135">筆記</span><span class="sxs-lookup"><span data-stu-id="fd963-135">NOTES</span></span>

## <span data-ttu-id="fd963-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="fd963-136">RELATED LINKS</span></span>

[<span data-ttu-id="fd963-137">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="fd963-137">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="fd963-138">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="fd963-138">Stop-AzDataFactoryV2Trigger</span></span>]()

