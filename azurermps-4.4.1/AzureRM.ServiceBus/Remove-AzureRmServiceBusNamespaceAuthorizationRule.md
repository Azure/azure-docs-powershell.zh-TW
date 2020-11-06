---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: 08f7f33138ddf9d5226cfc93f263fdec65de3388
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447988"
---
# <span data-ttu-id="ce80e-101">Remove-AzureRmServiceBusNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ce80e-101">Remove-AzureRmServiceBusNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="ce80e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ce80e-102">SYNOPSIS</span></span>
<span data-ttu-id="ce80e-103">從指定的資源群組中移除服務匯流排命名空間的授權規則。</span><span class="sxs-lookup"><span data-stu-id="ce80e-103">Removes the authorization rule of a Service Bus namespace from the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce80e-104">句法</span><span class="sxs-lookup"><span data-stu-id="ce80e-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroupName <String> -Namespace <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce80e-105">說明</span><span class="sxs-lookup"><span data-stu-id="ce80e-105">DESCRIPTION</span></span>
<span data-ttu-id="ce80e-106">**AzureRmServiceBusNamespaceAuthorizationRule** Cmdlet 會移除指定資源群組的服務匯流排命名空間的授權規則。</span><span class="sxs-lookup"><span data-stu-id="ce80e-106">The **Remove-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace for the specified resource group.</span></span>

## <span data-ttu-id="ce80e-107">示例</span><span class="sxs-lookup"><span data-stu-id="ce80e-107">EXAMPLES</span></span>

### <span data-ttu-id="ce80e-108">範例1</span><span class="sxs-lookup"><span data-stu-id="ce80e-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1
```

<span data-ttu-id="ce80e-109">`SBAuthoRule1` `SB-Example1` 從指定的資源群組中移除命名空間的授權規則。</span><span class="sxs-lookup"><span data-stu-id="ce80e-109">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

## <span data-ttu-id="ce80e-110">參數</span><span class="sxs-lookup"><span data-stu-id="ce80e-110">PARAMETERS</span></span>

### <span data-ttu-id="ce80e-111">-確認</span><span class="sxs-lookup"><span data-stu-id="ce80e-111">-Confirm</span></span>
<span data-ttu-id="ce80e-112">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ce80e-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce80e-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce80e-113">-WhatIf</span></span>
<span data-ttu-id="ce80e-114">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ce80e-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce80e-115">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce80e-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce80e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce80e-116">-DefaultProfile</span></span>
<span data-ttu-id="ce80e-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ce80e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce80e-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="ce80e-118">-Name</span></span>
<span data-ttu-id="ce80e-119">命名空間 AuthorizationRule 名稱。</span><span class="sxs-lookup"><span data-stu-id="ce80e-119">Namespace AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce80e-120">-命名空間</span><span class="sxs-lookup"><span data-stu-id="ce80e-120">-Namespace</span></span>
<span data-ttu-id="ce80e-121">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="ce80e-121">Namespace Name.</span></span>

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

### <span data-ttu-id="ce80e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce80e-122">-ResourceGroupName</span></span>
<span data-ttu-id="ce80e-123">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="ce80e-123">The name of the resource group</span></span>

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

### <span data-ttu-id="ce80e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce80e-124">CommonParameters</span></span>
<span data-ttu-id="ce80e-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ce80e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce80e-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ce80e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce80e-127">輸入</span><span class="sxs-lookup"><span data-stu-id="ce80e-127">INPUTS</span></span>

### <span data-ttu-id="ce80e-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ce80e-128">-ResourceGroup</span></span>
 <span data-ttu-id="ce80e-129">System.object</span><span class="sxs-lookup"><span data-stu-id="ce80e-129">System.String</span></span>

### <span data-ttu-id="ce80e-130">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="ce80e-130">-NamespaceName</span></span>
 <span data-ttu-id="ce80e-131">System.object</span><span class="sxs-lookup"><span data-stu-id="ce80e-131">System.String</span></span>

### <span data-ttu-id="ce80e-132">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="ce80e-132">-AuthorizationRuleName</span></span>
 <span data-ttu-id="ce80e-133">System.object</span><span class="sxs-lookup"><span data-stu-id="ce80e-133">System.String</span></span>

## <span data-ttu-id="ce80e-134">輸出</span><span class="sxs-lookup"><span data-stu-id="ce80e-134">OUTPUTS</span></span>

### <span data-ttu-id="ce80e-135">System.object</span><span class="sxs-lookup"><span data-stu-id="ce80e-135">System.Boolean</span></span>

## <span data-ttu-id="ce80e-136">筆記</span><span class="sxs-lookup"><span data-stu-id="ce80e-136">NOTES</span></span>

## <span data-ttu-id="ce80e-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="ce80e-137">RELATED LINKS</span></span>

