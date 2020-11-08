---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: 89fb4591af19db46aa536ebd15f3746cf6691244
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128468"
---
# <span data-ttu-id="fe772-101">Remove-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="fe772-101">Remove-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="fe772-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fe772-102">SYNOPSIS</span></span>
<span data-ttu-id="fe772-103">將事件觸發程式取消訂閱至外部服務事件。</span><span class="sxs-lookup"><span data-stu-id="fe772-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="fe772-104">句法</span><span class="sxs-lookup"><span data-stu-id="fe772-104">SYNTAX</span></span>

### <span data-ttu-id="fe772-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="fe772-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-Name] <String> [-PassThru] [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fe772-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fe772-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe772-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fe772-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-PassThru] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe772-108">說明</span><span class="sxs-lookup"><span data-stu-id="fe772-108">DESCRIPTION</span></span>
<span data-ttu-id="fe772-109">這個命令會將事件觸發程式從觸發程式的指定取消訂閱至指定的外部服務事件。</span><span class="sxs-lookup"><span data-stu-id="fe772-109">This command unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="fe772-110">示例</span><span class="sxs-lookup"><span data-stu-id="fe772-110">EXAMPLES</span></span>

### <span data-ttu-id="fe772-111">範例1</span><span class="sxs-lookup"><span data-stu-id="fe772-111">Example 1</span></span>
```
PS C:\> Remove-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1
```

<span data-ttu-id="fe772-112">這個命令會將 BlobEnetTrigger1 觸發程式取消訂閱至觸發程式的指定事件。</span><span class="sxs-lookup"><span data-stu-id="fe772-112">This command will unsubscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="fe772-113">參數</span><span class="sxs-lookup"><span data-stu-id="fe772-113">PARAMETERS</span></span>

### <span data-ttu-id="fe772-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="fe772-114">-DataFactoryName</span></span>
<span data-ttu-id="fe772-115">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="fe772-115">The data factory name.</span></span>

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

### <span data-ttu-id="fe772-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe772-116">-DefaultProfile</span></span>
<span data-ttu-id="fe772-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fe772-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe772-118">-Force</span><span class="sxs-lookup"><span data-stu-id="fe772-118">-Force</span></span>
<span data-ttu-id="fe772-119">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="fe772-119">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe772-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe772-120">-InputObject</span></span>
<span data-ttu-id="fe772-121">觸發程式物件。</span><span class="sxs-lookup"><span data-stu-id="fe772-121">The trigger object.</span></span>

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

### <span data-ttu-id="fe772-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="fe772-122">-Name</span></span>
<span data-ttu-id="fe772-123">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="fe772-123">The trigger name.</span></span>

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

### <span data-ttu-id="fe772-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe772-124">-PassThru</span></span>
<span data-ttu-id="fe772-125">如果已指定，則在成功刪除時，Cmdlet 會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="fe772-125">If specified, cmdlet will return return true on successful delete.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe772-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe772-126">-ResourceGroupName</span></span>
<span data-ttu-id="fe772-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fe772-127">The resource group name.</span></span>

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

### <span data-ttu-id="fe772-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe772-128">-ResourceId</span></span>
<span data-ttu-id="fe772-129">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="fe772-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="fe772-130">-確認</span><span class="sxs-lookup"><span data-stu-id="fe772-130">-Confirm</span></span>
<span data-ttu-id="fe772-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fe772-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe772-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe772-132">-WhatIf</span></span>
<span data-ttu-id="fe772-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fe772-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe772-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fe772-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe772-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe772-135">CommonParameters</span></span>
<span data-ttu-id="fe772-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fe772-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe772-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fe772-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe772-138">輸入</span><span class="sxs-lookup"><span data-stu-id="fe772-138">INPUTS</span></span>

### <span data-ttu-id="fe772-139">System.object</span><span class="sxs-lookup"><span data-stu-id="fe772-139">System.String</span></span>
<span data-ttu-id="fe772-140">PSTrigger 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="fe772-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="fe772-141">輸出</span><span class="sxs-lookup"><span data-stu-id="fe772-141">OUTPUTS</span></span>

### <span data-ttu-id="fe772-142">PSTriggerSubscriptionStatus 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="fe772-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="fe772-143">筆記</span><span class="sxs-lookup"><span data-stu-id="fe772-143">NOTES</span></span>

## <span data-ttu-id="fe772-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="fe772-144">RELATED LINKS</span></span>

