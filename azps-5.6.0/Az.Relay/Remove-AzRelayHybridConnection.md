---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/remove-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayHybridConnection.md
ms.openlocfilehash: b426eda2ab7e9714cd46a95c25d248adef5464a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914570"
---
# <span data-ttu-id="a5266-101">Remove-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="a5266-101">Remove-AzRelayHybridConnection</span></span>

## <span data-ttu-id="a5266-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a5266-102">SYNOPSIS</span></span>
<span data-ttu-id="a5266-103">從指定的 HybridConnection 命名空間移除 HybridConnection。</span><span class="sxs-lookup"><span data-stu-id="a5266-103">Removes the HybridConnection from the specified HybridConnection namespace.</span></span>

## <span data-ttu-id="a5266-104">語法</span><span class="sxs-lookup"><span data-stu-id="a5266-104">SYNTAX</span></span>

```
Remove-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5266-105">描述</span><span class="sxs-lookup"><span data-stu-id="a5266-105">DESCRIPTION</span></span>
<span data-ttu-id="a5266-106">**Remove-AzRelayHybridConnection** Cmdlet 會從指定的 Relay 命名空間移除 HybridConnection。</span><span class="sxs-lookup"><span data-stu-id="a5266-106">The **Remove-AzRelayHybridConnection** cmdlet removes the HybridConnection from the specified Relay namespace.</span></span>

## <span data-ttu-id="a5266-107">例子</span><span class="sxs-lookup"><span data-stu-id="a5266-107">EXAMPLES</span></span>

### <span data-ttu-id="a5266-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="a5266-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="a5266-109">移除命名空間中的 `TestHybridConnection` `TestNameSpace-Relay1` HybridConnection。</span><span class="sxs-lookup"><span data-stu-id="a5266-109">Removes the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="a5266-110">參數</span><span class="sxs-lookup"><span data-stu-id="a5266-110">PARAMETERS</span></span>

### <span data-ttu-id="a5266-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5266-111">-DefaultProfile</span></span>
<span data-ttu-id="a5266-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a5266-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5266-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="a5266-113">-Name</span></span>
<span data-ttu-id="a5266-114">HybridConnections Name.</span><span class="sxs-lookup"><span data-stu-id="a5266-114">HybridConnections Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5266-115">-命名空間</span><span class="sxs-lookup"><span data-stu-id="a5266-115">-Namespace</span></span>
<span data-ttu-id="a5266-116">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="a5266-116">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5266-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5266-117">-ResourceGroupName</span></span>
<span data-ttu-id="a5266-118">資源組名。</span><span class="sxs-lookup"><span data-stu-id="a5266-118">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5266-119">-確認</span><span class="sxs-lookup"><span data-stu-id="a5266-119">-Confirm</span></span>
<span data-ttu-id="a5266-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a5266-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5266-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5266-121">-WhatIf</span></span>
<span data-ttu-id="a5266-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a5266-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5266-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a5266-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5266-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5266-124">CommonParameters</span></span>
<span data-ttu-id="a5266-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a5266-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5266-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a5266-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5266-127">輸入</span><span class="sxs-lookup"><span data-stu-id="a5266-127">INPUTS</span></span>

### <span data-ttu-id="a5266-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a5266-128">System.String</span></span>

## <span data-ttu-id="a5266-129">輸出</span><span class="sxs-lookup"><span data-stu-id="a5266-129">OUTPUTS</span></span>

### <span data-ttu-id="a5266-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="a5266-130">System.Void</span></span>

## <span data-ttu-id="a5266-131">筆記</span><span class="sxs-lookup"><span data-stu-id="a5266-131">NOTES</span></span>

## <span data-ttu-id="a5266-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="a5266-132">RELATED LINKS</span></span>
