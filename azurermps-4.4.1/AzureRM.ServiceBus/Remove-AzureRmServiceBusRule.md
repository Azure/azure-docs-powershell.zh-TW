---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusRule.md
ms.openlocfilehash: 287a0b82c9236841b613ac52a7a07ccf8adb4811
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447979"
---
# <span data-ttu-id="276c7-101">Remove-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="276c7-101">Remove-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="276c7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="276c7-102">SYNOPSIS</span></span>
<span data-ttu-id="276c7-103">移除指定訂閱的指定規則。</span><span class="sxs-lookup"><span data-stu-id="276c7-103">Removes the speficied rule of a given subscription .</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="276c7-104">句法</span><span class="sxs-lookup"><span data-stu-id="276c7-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="276c7-105">說明</span><span class="sxs-lookup"><span data-stu-id="276c7-105">DESCRIPTION</span></span>
<span data-ttu-id="276c7-106">**AzureRmServiceBusRule** Cmdlet 會移除指定主題的訂閱規則。</span><span class="sxs-lookup"><span data-stu-id="276c7-106">The **Remove-AzureRmServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="276c7-107">示例</span><span class="sxs-lookup"><span data-stu-id="276c7-107">EXAMPLES</span></span>

### <span data-ttu-id="276c7-108">範例1</span><span class="sxs-lookup"><span data-stu-id="276c7-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="276c7-109">移除 `SBRule` 指定主題的訂閱規則 `SBSubscription` `SBTopic` 。</span><span class="sxs-lookup"><span data-stu-id="276c7-109">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

## <span data-ttu-id="276c7-110">參數</span><span class="sxs-lookup"><span data-stu-id="276c7-110">PARAMETERS</span></span>

### <span data-ttu-id="276c7-111">-確認</span><span class="sxs-lookup"><span data-stu-id="276c7-111">-Confirm</span></span>
<span data-ttu-id="276c7-112">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="276c7-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="276c7-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="276c7-113">-Name</span></span>
<span data-ttu-id="276c7-114">規則名稱。</span><span class="sxs-lookup"><span data-stu-id="276c7-114">Rule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="276c7-115">-命名空間</span><span class="sxs-lookup"><span data-stu-id="276c7-115">-Namespace</span></span>
<span data-ttu-id="276c7-116">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="276c7-116">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="276c7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="276c7-117">-ResourceGroupName</span></span>
<span data-ttu-id="276c7-118">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="276c7-118">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="276c7-119">-訂閱</span><span class="sxs-lookup"><span data-stu-id="276c7-119">-Subscription</span></span>
<span data-ttu-id="276c7-120">訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="276c7-120">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="276c7-121">-主題</span><span class="sxs-lookup"><span data-stu-id="276c7-121">-Topic</span></span>
<span data-ttu-id="276c7-122">主題名稱。</span><span class="sxs-lookup"><span data-stu-id="276c7-122">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="276c7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="276c7-123">-WhatIf</span></span>
<span data-ttu-id="276c7-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="276c7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="276c7-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="276c7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="276c7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="276c7-126">-DefaultProfile</span></span>
<span data-ttu-id="276c7-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="276c7-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="276c7-128">-Force</span><span class="sxs-lookup"><span data-stu-id="276c7-128">-Force</span></span>
<span data-ttu-id="276c7-129">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="276c7-129">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="276c7-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="276c7-130">-PassThru</span></span>
<span data-ttu-id="276c7-131">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="276c7-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="276c7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="276c7-132">CommonParameters</span></span>
<span data-ttu-id="276c7-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="276c7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="276c7-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="276c7-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="276c7-135">輸入</span><span class="sxs-lookup"><span data-stu-id="276c7-135">INPUTS</span></span>

### <span data-ttu-id="276c7-136">System.object</span><span class="sxs-lookup"><span data-stu-id="276c7-136">System.String</span></span>

## <span data-ttu-id="276c7-137">輸出</span><span class="sxs-lookup"><span data-stu-id="276c7-137">OUTPUTS</span></span>

### <span data-ttu-id="276c7-138">System.object</span><span class="sxs-lookup"><span data-stu-id="276c7-138">System.Boolean</span></span>

## <span data-ttu-id="276c7-139">筆記</span><span class="sxs-lookup"><span data-stu-id="276c7-139">NOTES</span></span>

## <span data-ttu-id="276c7-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="276c7-140">RELATED LINKS</span></span>

