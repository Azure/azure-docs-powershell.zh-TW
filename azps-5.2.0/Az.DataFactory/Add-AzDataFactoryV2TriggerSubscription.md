---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/add-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: 6e38f98f9dd3ebfaa2ad4747016556aecd9998e9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274751"
---
# <span data-ttu-id="edca0-101">Add-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="edca0-101">Add-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="edca0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="edca0-102">SYNOPSIS</span></span>
<span data-ttu-id="edca0-103">為外部服務事件訂閱事件觸發程式。</span><span class="sxs-lookup"><span data-stu-id="edca0-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="edca0-104">句法</span><span class="sxs-lookup"><span data-stu-id="edca0-104">SYNTAX</span></span>

### <span data-ttu-id="edca0-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="edca0-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="edca0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="edca0-106">ByInputObject</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edca0-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="edca0-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edca0-108">說明</span><span class="sxs-lookup"><span data-stu-id="edca0-108">DESCRIPTION</span></span>
<span data-ttu-id="edca0-109">這個命令會從觸發程式的指定，將事件觸發程式訂閱至指定的外部服務事件。</span><span class="sxs-lookup"><span data-stu-id="edca0-109">This command subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="edca0-110">示例</span><span class="sxs-lookup"><span data-stu-id="edca0-110">EXAMPLES</span></span>

### <span data-ttu-id="edca0-111">範例1</span><span class="sxs-lookup"><span data-stu-id="edca0-111">Example 1</span></span>
```
PS C:\> Add-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Provisioning
```

<span data-ttu-id="edca0-112">這個命令會從觸發程式的指定，將 BlobEnetTrigger1 觸發程式訂閱至指定事件。</span><span class="sxs-lookup"><span data-stu-id="edca0-112">This command will subscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="edca0-113">參數</span><span class="sxs-lookup"><span data-stu-id="edca0-113">PARAMETERS</span></span>

### <span data-ttu-id="edca0-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="edca0-114">-DataFactoryName</span></span>
<span data-ttu-id="edca0-115">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="edca0-115">The data factory name.</span></span>

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

### <span data-ttu-id="edca0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edca0-116">-DefaultProfile</span></span>
<span data-ttu-id="edca0-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="edca0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edca0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="edca0-118">-InputObject</span></span>
<span data-ttu-id="edca0-119">觸發程式物件。</span><span class="sxs-lookup"><span data-stu-id="edca0-119">The trigger object.</span></span>

```yaml
Type: PSTrigger
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="edca0-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="edca0-120">-Name</span></span>
<span data-ttu-id="edca0-121">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="edca0-121">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edca0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edca0-122">-ResourceGroupName</span></span>
<span data-ttu-id="edca0-123">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="edca0-123">The resource group name.</span></span>

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

### <span data-ttu-id="edca0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="edca0-124">-ResourceId</span></span>
<span data-ttu-id="edca0-125">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="edca0-125">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edca0-126">-確認</span><span class="sxs-lookup"><span data-stu-id="edca0-126">-Confirm</span></span>
<span data-ttu-id="edca0-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="edca0-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edca0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edca0-128">-WhatIf</span></span>
<span data-ttu-id="edca0-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="edca0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edca0-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="edca0-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edca0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edca0-131">CommonParameters</span></span>
<span data-ttu-id="edca0-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="edca0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edca0-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="edca0-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edca0-134">輸入</span><span class="sxs-lookup"><span data-stu-id="edca0-134">INPUTS</span></span>

### <span data-ttu-id="edca0-135">System.object</span><span class="sxs-lookup"><span data-stu-id="edca0-135">System.String</span></span>
<span data-ttu-id="edca0-136">PSTrigger 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="edca0-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="edca0-137">輸出</span><span class="sxs-lookup"><span data-stu-id="edca0-137">OUTPUTS</span></span>

### <span data-ttu-id="edca0-138">PSTriggerSubscriptionStatus 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="edca0-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="edca0-139">筆記</span><span class="sxs-lookup"><span data-stu-id="edca0-139">NOTES</span></span>

## <span data-ttu-id="edca0-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="edca0-140">RELATED LINKS</span></span>

