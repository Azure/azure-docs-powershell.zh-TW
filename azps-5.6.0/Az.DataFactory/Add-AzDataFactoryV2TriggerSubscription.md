---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/add-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: c74eb60e698cff0d95a4361235c9282f1405dce0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912425"
---
# <span data-ttu-id="f2cf3-101">Add-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="f2cf3-101">Add-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="f2cf3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f2cf3-102">SYNOPSIS</span></span>
<span data-ttu-id="f2cf3-103">訂閱事件觸發事件至外部服務事件。</span><span class="sxs-lookup"><span data-stu-id="f2cf3-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="f2cf3-104">語法</span><span class="sxs-lookup"><span data-stu-id="f2cf3-104">SYNTAX</span></span>

### <span data-ttu-id="f2cf3-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="f2cf3-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f2cf3-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f2cf3-106">ByInputObject</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2cf3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f2cf3-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2cf3-108">描述</span><span class="sxs-lookup"><span data-stu-id="f2cf3-108">DESCRIPTION</span></span>
<span data-ttu-id="f2cf3-109">此命令會訂閱觸發者所指定外部服務事件的事件觸發。</span><span class="sxs-lookup"><span data-stu-id="f2cf3-109">This command subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="f2cf3-110">例子</span><span class="sxs-lookup"><span data-stu-id="f2cf3-110">EXAMPLES</span></span>

### <span data-ttu-id="f2cf3-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="f2cf3-111">Example 1</span></span>
```
PS C:\> Add-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Provisioning
```

<span data-ttu-id="f2cf3-112">此命令會訂閱 BlobEnetTrigger1 觸發程式從觸發程式觸發指定事件。</span><span class="sxs-lookup"><span data-stu-id="f2cf3-112">This command will subscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="f2cf3-113">參數</span><span class="sxs-lookup"><span data-stu-id="f2cf3-113">PARAMETERS</span></span>

### <span data-ttu-id="f2cf3-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f2cf3-114">-DataFactoryName</span></span>
<span data-ttu-id="f2cf3-115">資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="f2cf3-115">The data factory name.</span></span>

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

### <span data-ttu-id="f2cf3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2cf3-116">-DefaultProfile</span></span>
<span data-ttu-id="f2cf3-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f2cf3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2cf3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2cf3-118">-InputObject</span></span>
<span data-ttu-id="f2cf3-119">觸發物件。</span><span class="sxs-lookup"><span data-stu-id="f2cf3-119">The trigger object.</span></span>

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

### <span data-ttu-id="f2cf3-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="f2cf3-120">-Name</span></span>
<span data-ttu-id="f2cf3-121">觸發者名稱。</span><span class="sxs-lookup"><span data-stu-id="f2cf3-121">The trigger name.</span></span>

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

### <span data-ttu-id="f2cf3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2cf3-122">-ResourceGroupName</span></span>
<span data-ttu-id="f2cf3-123">資源組名。</span><span class="sxs-lookup"><span data-stu-id="f2cf3-123">The resource group name.</span></span>

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

### <span data-ttu-id="f2cf3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2cf3-124">-ResourceId</span></span>
<span data-ttu-id="f2cf3-125">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f2cf3-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="f2cf3-126">-確認</span><span class="sxs-lookup"><span data-stu-id="f2cf3-126">-Confirm</span></span>
<span data-ttu-id="f2cf3-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f2cf3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2cf3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2cf3-128">-WhatIf</span></span>
<span data-ttu-id="f2cf3-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f2cf3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2cf3-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f2cf3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2cf3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2cf3-131">CommonParameters</span></span>
<span data-ttu-id="f2cf3-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f2cf3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2cf3-133">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f2cf3-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2cf3-134">輸入</span><span class="sxs-lookup"><span data-stu-id="f2cf3-134">INPUTS</span></span>

### <span data-ttu-id="f2cf3-135">System.String</span><span class="sxs-lookup"><span data-stu-id="f2cf3-135">System.String</span></span>
<span data-ttu-id="f2cf3-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="f2cf3-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="f2cf3-137">輸出</span><span class="sxs-lookup"><span data-stu-id="f2cf3-137">OUTPUTS</span></span>

### <span data-ttu-id="f2cf3-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="f2cf3-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="f2cf3-139">筆記</span><span class="sxs-lookup"><span data-stu-id="f2cf3-139">NOTES</span></span>

## <span data-ttu-id="f2cf3-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2cf3-140">RELATED LINKS</span></span>

