---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
ms.openlocfilehash: 356140c964280634f469dd9b9955adaf62130090
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446659"
---
# <span data-ttu-id="84821-101">Remove-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="84821-101">Remove-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="84821-102">摘要</span><span class="sxs-lookup"><span data-stu-id="84821-102">SYNOPSIS</span></span>
<span data-ttu-id="84821-103">從指定的服務匯流排命名空間中移除主題。</span><span class="sxs-lookup"><span data-stu-id="84821-103">Removes the topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84821-104">句法</span><span class="sxs-lookup"><span data-stu-id="84821-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusTopic -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84821-105">說明</span><span class="sxs-lookup"><span data-stu-id="84821-105">DESCRIPTION</span></span>
<span data-ttu-id="84821-106">**AzureRmServiceBusTopic** Cmdlet 會從指定的服務匯流排命名空間中移除主題。</span><span class="sxs-lookup"><span data-stu-id="84821-106">The **Remove-AzureRmServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="84821-107">示例</span><span class="sxs-lookup"><span data-stu-id="84821-107">EXAMPLES</span></span>

### <span data-ttu-id="84821-108">範例1</span><span class="sxs-lookup"><span data-stu-id="84821-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="84821-109">移除 `SB-Topic_exampl1` 命名空間中的主題 `SB-Example1` 。</span><span class="sxs-lookup"><span data-stu-id="84821-109">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="84821-110">參數</span><span class="sxs-lookup"><span data-stu-id="84821-110">PARAMETERS</span></span>

### <span data-ttu-id="84821-111">-確認</span><span class="sxs-lookup"><span data-stu-id="84821-111">-Confirm</span></span>
<span data-ttu-id="84821-112">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="84821-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84821-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84821-113">-WhatIf</span></span>
<span data-ttu-id="84821-114">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="84821-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84821-115">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="84821-115">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84821-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84821-116">-DefaultProfile</span></span>
<span data-ttu-id="84821-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="84821-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84821-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="84821-118">-Name</span></span>
<span data-ttu-id="84821-119">主題名稱。</span><span class="sxs-lookup"><span data-stu-id="84821-119">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84821-120">-命名空間</span><span class="sxs-lookup"><span data-stu-id="84821-120">-Namespace</span></span>
<span data-ttu-id="84821-121">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="84821-121">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84821-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84821-122">-ResourceGroupName</span></span>
<span data-ttu-id="84821-123">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="84821-123">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84821-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84821-124">CommonParameters</span></span>
<span data-ttu-id="84821-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="84821-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84821-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="84821-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84821-127">輸入</span><span class="sxs-lookup"><span data-stu-id="84821-127">INPUTS</span></span>

### <span data-ttu-id="84821-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="84821-128">-ResourceGroup</span></span>
 <span data-ttu-id="84821-129">System.object</span><span class="sxs-lookup"><span data-stu-id="84821-129">System.String</span></span>

### <span data-ttu-id="84821-130">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="84821-130">-NamespaceName</span></span>
 <span data-ttu-id="84821-131">System.object</span><span class="sxs-lookup"><span data-stu-id="84821-131">System.String</span></span>

### <span data-ttu-id="84821-132">-TopicName</span><span class="sxs-lookup"><span data-stu-id="84821-132">-TopicName</span></span>
 <span data-ttu-id="84821-133">System.object</span><span class="sxs-lookup"><span data-stu-id="84821-133">System.String</span></span>

## <span data-ttu-id="84821-134">輸出</span><span class="sxs-lookup"><span data-stu-id="84821-134">OUTPUTS</span></span>

### <span data-ttu-id="84821-135">System.object</span><span class="sxs-lookup"><span data-stu-id="84821-135">System.Object</span></span>

## <span data-ttu-id="84821-136">筆記</span><span class="sxs-lookup"><span data-stu-id="84821-136">NOTES</span></span>

## <span data-ttu-id="84821-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="84821-137">RELATED LINKS</span></span>

