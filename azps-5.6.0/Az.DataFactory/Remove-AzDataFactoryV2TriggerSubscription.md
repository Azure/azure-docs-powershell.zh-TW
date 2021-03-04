---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: 1ab801c9eca278d5d117ddca881867371882980c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913569"
---
# <span data-ttu-id="01db6-101">Remove-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="01db6-101">Remove-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="01db6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="01db6-102">SYNOPSIS</span></span>
<span data-ttu-id="01db6-103">取消訂閱外部服務事件的事件觸發。</span><span class="sxs-lookup"><span data-stu-id="01db6-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="01db6-104">語法</span><span class="sxs-lookup"><span data-stu-id="01db6-104">SYNTAX</span></span>

### <span data-ttu-id="01db6-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="01db6-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-Name] <String> [-PassThru] [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01db6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="01db6-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01db6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="01db6-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-PassThru] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01db6-108">描述</span><span class="sxs-lookup"><span data-stu-id="01db6-108">DESCRIPTION</span></span>
<span data-ttu-id="01db6-109">此命令會取消訂閱觸發者對指定外部服務事件的事件觸發。</span><span class="sxs-lookup"><span data-stu-id="01db6-109">This command unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="01db6-110">例子</span><span class="sxs-lookup"><span data-stu-id="01db6-110">EXAMPLES</span></span>

### <span data-ttu-id="01db6-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="01db6-111">Example 1</span></span>
```
PS C:\> Remove-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1
```

<span data-ttu-id="01db6-112">此命令會取消訂閱 BlobEnetTrigger1 觸發程式從觸發程式觸發指定事件。</span><span class="sxs-lookup"><span data-stu-id="01db6-112">This command will unsubscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="01db6-113">參數</span><span class="sxs-lookup"><span data-stu-id="01db6-113">PARAMETERS</span></span>

### <span data-ttu-id="01db6-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="01db6-114">-DataFactoryName</span></span>
<span data-ttu-id="01db6-115">資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="01db6-115">The data factory name.</span></span>

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

### <span data-ttu-id="01db6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01db6-116">-DefaultProfile</span></span>
<span data-ttu-id="01db6-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="01db6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01db6-118">-強制</span><span class="sxs-lookup"><span data-stu-id="01db6-118">-Force</span></span>
<span data-ttu-id="01db6-119">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="01db6-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="01db6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01db6-120">-InputObject</span></span>
<span data-ttu-id="01db6-121">觸發物件。</span><span class="sxs-lookup"><span data-stu-id="01db6-121">The trigger object.</span></span>

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

### <span data-ttu-id="01db6-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="01db6-122">-Name</span></span>
<span data-ttu-id="01db6-123">觸發者名稱。</span><span class="sxs-lookup"><span data-stu-id="01db6-123">The trigger name.</span></span>

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

### <span data-ttu-id="01db6-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01db6-124">-PassThru</span></span>
<span data-ttu-id="01db6-125">如果指定，Cmdlet 在成功刪除時會返回 true。</span><span class="sxs-lookup"><span data-stu-id="01db6-125">If specified, cmdlet will return return true on successful delete.</span></span>

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

### <span data-ttu-id="01db6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01db6-126">-ResourceGroupName</span></span>
<span data-ttu-id="01db6-127">資源組名。</span><span class="sxs-lookup"><span data-stu-id="01db6-127">The resource group name.</span></span>

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

### <span data-ttu-id="01db6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01db6-128">-ResourceId</span></span>
<span data-ttu-id="01db6-129">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="01db6-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="01db6-130">-確認</span><span class="sxs-lookup"><span data-stu-id="01db6-130">-Confirm</span></span>
<span data-ttu-id="01db6-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="01db6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01db6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01db6-132">-WhatIf</span></span>
<span data-ttu-id="01db6-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="01db6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01db6-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="01db6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01db6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01db6-135">CommonParameters</span></span>
<span data-ttu-id="01db6-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="01db6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01db6-137">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="01db6-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01db6-138">輸入</span><span class="sxs-lookup"><span data-stu-id="01db6-138">INPUTS</span></span>

### <span data-ttu-id="01db6-139">System.String</span><span class="sxs-lookup"><span data-stu-id="01db6-139">System.String</span></span>
<span data-ttu-id="01db6-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="01db6-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="01db6-141">輸出</span><span class="sxs-lookup"><span data-stu-id="01db6-141">OUTPUTS</span></span>

### <span data-ttu-id="01db6-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="01db6-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="01db6-143">筆記</span><span class="sxs-lookup"><span data-stu-id="01db6-143">NOTES</span></span>

## <span data-ttu-id="01db6-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="01db6-144">RELATED LINKS</span></span>

