---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: dc4630359070e627a3c65c63f21c23f987cb9a31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449207"
---
# <span data-ttu-id="e1414-101">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="e1414-101">Set-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="e1414-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e1414-102">SYNOPSIS</span></span>
<span data-ttu-id="e1414-103">在資料工廠中建立觸發程式。</span><span class="sxs-lookup"><span data-stu-id="e1414-103">Creates a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1414-104">句法</span><span class="sxs-lookup"><span data-stu-id="e1414-104">SYNTAX</span></span>

### <span data-ttu-id="e1414-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="e1414-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Trigger [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e1414-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e1414-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Trigger [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1414-107">說明</span><span class="sxs-lookup"><span data-stu-id="e1414-107">DESCRIPTION</span></span>
<span data-ttu-id="e1414-108">**AzureRmDataFactoryV2Trigger** Cmdlet 會在資料工廠中建立觸發程式。</span><span class="sxs-lookup"><span data-stu-id="e1414-108">The **Set-AzureRmDataFactoryV2Trigger** cmdlet creates a trigger in a data factory.</span></span> <span data-ttu-id="e1414-109">如果您指定已存在之觸發程式的名稱，此 Cmdlet 會在您取代觸發程式之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e1414-109">If you specify a name for a trigger that already exists, the cmdlet prompts for confirmation before replacing the trigger.</span></span> <span data-ttu-id="e1414-110">如果您指定 _Force_ 參數，則 Cmdlet 會取代現有的觸發程式，而不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e1414-110">If you specify the _Force_ parameter, the cmdlet replaces the existing trigger without prompting for confirmation.</span></span> <span data-ttu-id="e1414-111">觸發程式是在「已停止」狀態中建立，這表示它們不會立即開始喚醒它們所參照的管線。</span><span class="sxs-lookup"><span data-stu-id="e1414-111">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="e1414-112">示例</span><span class="sxs-lookup"><span data-stu-id="e1414-112">EXAMPLES</span></span>

### <span data-ttu-id="e1414-113">範例1：建立觸發程式</span><span class="sxs-lookup"><span data-stu-id="e1414-113">Example 1: Create a trigger</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger" -DefinitionFile ".\scheduledTrigger.json"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="e1414-114">在資料工廠 "WikiADF" 中，建立一個名為 "ScheduledTrigger" 的新觸發程式。</span><span class="sxs-lookup"><span data-stu-id="e1414-114">Create a new trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span> <span data-ttu-id="e1414-115">觸發程式是以「已停止」狀態建立，表示它不會立即啟動。</span><span class="sxs-lookup"><span data-stu-id="e1414-115">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="e1414-116">您可以使用 Cmdlet 來啟動觸發程式 `Start-AzureRmDataFactoryV2Trigger` 。</span><span class="sxs-lookup"><span data-stu-id="e1414-116">A trigger can be started using the `Start-AzureRmDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="e1414-117">參數</span><span class="sxs-lookup"><span data-stu-id="e1414-117">PARAMETERS</span></span>

### <span data-ttu-id="e1414-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e1414-118">-DataFactoryName</span></span>
<span data-ttu-id="e1414-119">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="e1414-119">The data factory name.</span></span>

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

### <span data-ttu-id="e1414-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1414-120">-DefaultProfile</span></span>
<span data-ttu-id="e1414-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e1414-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1414-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="e1414-122">-DefinitionFile</span></span>
<span data-ttu-id="e1414-123">JSON 檔路徑。</span><span class="sxs-lookup"><span data-stu-id="e1414-123">The JSON file path.</span></span>

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

### <span data-ttu-id="e1414-124">-Force</span><span class="sxs-lookup"><span data-stu-id="e1414-124">-Force</span></span>
<span data-ttu-id="e1414-125">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e1414-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="e1414-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="e1414-126">-Name</span></span>
<span data-ttu-id="e1414-127">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="e1414-127">The trigger name.</span></span>

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

### <span data-ttu-id="e1414-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1414-128">-ResourceGroupName</span></span>
<span data-ttu-id="e1414-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e1414-129">The resource group name.</span></span>

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

### <span data-ttu-id="e1414-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1414-130">-ResourceId</span></span>
<span data-ttu-id="e1414-131">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e1414-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="e1414-132">-確認</span><span class="sxs-lookup"><span data-stu-id="e1414-132">-Confirm</span></span>
<span data-ttu-id="e1414-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e1414-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1414-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1414-134">-WhatIf</span></span>
<span data-ttu-id="e1414-135">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e1414-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="e1414-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1414-136">CommonParameters</span></span>
<span data-ttu-id="e1414-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e1414-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1414-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e1414-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1414-139">輸入</span><span class="sxs-lookup"><span data-stu-id="e1414-139">INPUTS</span></span>

### <span data-ttu-id="e1414-140">System.object</span><span class="sxs-lookup"><span data-stu-id="e1414-140">System.String</span></span>

## <span data-ttu-id="e1414-141">輸出</span><span class="sxs-lookup"><span data-stu-id="e1414-141">OUTPUTS</span></span>

### <span data-ttu-id="e1414-142">PSTrigger 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="e1414-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="e1414-143">筆記</span><span class="sxs-lookup"><span data-stu-id="e1414-143">NOTES</span></span>

## <span data-ttu-id="e1414-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="e1414-144">RELATED LINKS</span></span>

[<span data-ttu-id="e1414-145">AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="e1414-145">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="e1414-146">開始-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="e1414-146">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="e1414-147">停止 AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="e1414-147">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="e1414-148">移除-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="e1414-148">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
