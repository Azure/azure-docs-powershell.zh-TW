---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Trigger.md
ms.openlocfilehash: b0058f21f472f14e97898ea81636fa000034bed5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916186"
---
# <span data-ttu-id="4946e-101">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="4946e-101">Set-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="4946e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4946e-102">SYNOPSIS</span></span>
<span data-ttu-id="4946e-103">在資料工廠中建立觸發。</span><span class="sxs-lookup"><span data-stu-id="4946e-103">Creates a trigger in a data factory.</span></span>

## <span data-ttu-id="4946e-104">語法</span><span class="sxs-lookup"><span data-stu-id="4946e-104">SYNTAX</span></span>

### <span data-ttu-id="4946e-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="4946e-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Trigger [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4946e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4946e-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Trigger [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4946e-107">描述</span><span class="sxs-lookup"><span data-stu-id="4946e-107">DESCRIPTION</span></span>
<span data-ttu-id="4946e-108">**Set-AzDataFactoryV2Trigger** Cmdlet 在資料工廠中建立觸發程式。</span><span class="sxs-lookup"><span data-stu-id="4946e-108">The **Set-AzDataFactoryV2Trigger** cmdlet creates a trigger in a data factory.</span></span> <span data-ttu-id="4946e-109">如果您為已存在的觸發專案指定名稱，Cmdlet 會先提示您確認，然後再取代觸發。</span><span class="sxs-lookup"><span data-stu-id="4946e-109">If you specify a name for a trigger that already exists, the cmdlet prompts for confirmation before replacing the trigger.</span></span> <span data-ttu-id="4946e-110">如果您指定 _Force_ 參數，Cmdlet 會取代現有的觸發程式，而不會提示確認。</span><span class="sxs-lookup"><span data-stu-id="4946e-110">If you specify the _Force_ parameter, the cmdlet replaces the existing trigger without prompting for confirmation.</span></span> <span data-ttu-id="4946e-111">觸發會以 '已停止' 狀態建立，這表示它們不會立即開始叫用他們參照的管道。</span><span class="sxs-lookup"><span data-stu-id="4946e-111">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="4946e-112">例子</span><span class="sxs-lookup"><span data-stu-id="4946e-112">EXAMPLES</span></span>

### <span data-ttu-id="4946e-113">範例 1：建立觸發</span><span class="sxs-lookup"><span data-stu-id="4946e-113">Example 1: Create a trigger</span></span>
```
PS C:\> Set-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger" -DefinitionFile ".\scheduledTrigger.json"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="4946e-114">在資料工廠的 「WikiADF」中建立名為「ScheduledTri用」的新觸發程式。</span><span class="sxs-lookup"><span data-stu-id="4946e-114">Create a new trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span> <span data-ttu-id="4946e-115">觸發會以 '已停止' 狀態建立，這表示它不會立即開始。</span><span class="sxs-lookup"><span data-stu-id="4946e-115">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="4946e-116">可以使用 `Start-AzDataFactoryV2Trigger` Cmdlet 啟動觸發程式。</span><span class="sxs-lookup"><span data-stu-id="4946e-116">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="4946e-117">參數</span><span class="sxs-lookup"><span data-stu-id="4946e-117">PARAMETERS</span></span>

### <span data-ttu-id="4946e-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4946e-118">-DataFactoryName</span></span>
<span data-ttu-id="4946e-119">資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="4946e-119">The data factory name.</span></span>

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

### <span data-ttu-id="4946e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4946e-120">-DefaultProfile</span></span>
<span data-ttu-id="4946e-121">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4946e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4946e-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="4946e-122">-DefinitionFile</span></span>
<span data-ttu-id="4946e-123">JSON 檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="4946e-123">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4946e-124">-強制</span><span class="sxs-lookup"><span data-stu-id="4946e-124">-Force</span></span>
<span data-ttu-id="4946e-125">執行 Cmdlet 而不提示確認。</span><span class="sxs-lookup"><span data-stu-id="4946e-125">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4946e-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="4946e-126">-Name</span></span>
<span data-ttu-id="4946e-127">觸發者名稱。</span><span class="sxs-lookup"><span data-stu-id="4946e-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4946e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4946e-128">-ResourceGroupName</span></span>
<span data-ttu-id="4946e-129">資源組名。</span><span class="sxs-lookup"><span data-stu-id="4946e-129">The resource group name.</span></span>

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

### <span data-ttu-id="4946e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4946e-130">-ResourceId</span></span>
<span data-ttu-id="4946e-131">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4946e-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="4946e-132">-確認</span><span class="sxs-lookup"><span data-stu-id="4946e-132">-Confirm</span></span>
<span data-ttu-id="4946e-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4946e-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4946e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4946e-134">-WhatIf</span></span>
<span data-ttu-id="4946e-135">顯示如果 Cmdlet 執行，但不執行 Cmdlet 會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4946e-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4946e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4946e-136">CommonParameters</span></span>
<span data-ttu-id="4946e-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4946e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4946e-138">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="4946e-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4946e-139">輸入</span><span class="sxs-lookup"><span data-stu-id="4946e-139">INPUTS</span></span>

### <span data-ttu-id="4946e-140">System.String</span><span class="sxs-lookup"><span data-stu-id="4946e-140">System.String</span></span>

## <span data-ttu-id="4946e-141">輸出</span><span class="sxs-lookup"><span data-stu-id="4946e-141">OUTPUTS</span></span>

### <span data-ttu-id="4946e-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="4946e-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="4946e-143">筆記</span><span class="sxs-lookup"><span data-stu-id="4946e-143">NOTES</span></span>

## <span data-ttu-id="4946e-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="4946e-144">RELATED LINKS</span></span>

[<span data-ttu-id="4946e-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="4946e-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="4946e-146">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="4946e-146">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="4946e-147">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="4946e-147">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="4946e-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="4946e-148">Remove-AzDataFactoryV2Trigger</span></span>]()
