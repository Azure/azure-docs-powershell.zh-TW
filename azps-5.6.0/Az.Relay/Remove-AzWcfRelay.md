---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/remove-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
ms.openlocfilehash: f99a3a999baad580e04c6872f047c02d4a99091f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914562"
---
# <span data-ttu-id="325a6-101">Remove-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="325a6-101">Remove-AzWcfRelay</span></span>

## <span data-ttu-id="325a6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="325a6-102">SYNOPSIS</span></span>
<span data-ttu-id="325a6-103">從指定的 Relay 命名空間移除 WcfRelay。</span><span class="sxs-lookup"><span data-stu-id="325a6-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="325a6-104">語法</span><span class="sxs-lookup"><span data-stu-id="325a6-104">SYNTAX</span></span>

```
Remove-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="325a6-105">描述</span><span class="sxs-lookup"><span data-stu-id="325a6-105">DESCRIPTION</span></span>
<span data-ttu-id="325a6-106">**Remove-AzWcfRelay** Cmdlet 會從指定的 Relay 命名空間移除 WcfRelay。</span><span class="sxs-lookup"><span data-stu-id="325a6-106">The **Remove-AzWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="325a6-107">例子</span><span class="sxs-lookup"><span data-stu-id="325a6-107">EXAMPLES</span></span>

### <span data-ttu-id="325a6-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="325a6-108">Example 1</span></span>
```
PS C:\> Remove-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="325a6-109">從命名空間移除 `TestWCFRelay1` `TestNameSpace-Relay1` WcfRelay。</span><span class="sxs-lookup"><span data-stu-id="325a6-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="325a6-110">參數</span><span class="sxs-lookup"><span data-stu-id="325a6-110">PARAMETERS</span></span>

### <span data-ttu-id="325a6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="325a6-111">-DefaultProfile</span></span>
<span data-ttu-id="325a6-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="325a6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="325a6-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="325a6-113">-Name</span></span>
<span data-ttu-id="325a6-114">WcfRelay 名稱。</span><span class="sxs-lookup"><span data-stu-id="325a6-114">WcfRelay Name.</span></span>

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

### <span data-ttu-id="325a6-115">-命名空間</span><span class="sxs-lookup"><span data-stu-id="325a6-115">-Namespace</span></span>
<span data-ttu-id="325a6-116">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="325a6-116">Namespace Name.</span></span>

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

### <span data-ttu-id="325a6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="325a6-117">-ResourceGroupName</span></span>
<span data-ttu-id="325a6-118">資源組名。</span><span class="sxs-lookup"><span data-stu-id="325a6-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="325a6-119">-確認</span><span class="sxs-lookup"><span data-stu-id="325a6-119">-Confirm</span></span>
<span data-ttu-id="325a6-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="325a6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="325a6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="325a6-121">-WhatIf</span></span>
<span data-ttu-id="325a6-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="325a6-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="325a6-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="325a6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="325a6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="325a6-124">CommonParameters</span></span>
<span data-ttu-id="325a6-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="325a6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="325a6-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="325a6-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="325a6-127">輸入</span><span class="sxs-lookup"><span data-stu-id="325a6-127">INPUTS</span></span>

### <span data-ttu-id="325a6-128">System.String</span><span class="sxs-lookup"><span data-stu-id="325a6-128">System.String</span></span>

## <span data-ttu-id="325a6-129">輸出</span><span class="sxs-lookup"><span data-stu-id="325a6-129">OUTPUTS</span></span>

### <span data-ttu-id="325a6-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="325a6-130">System.Void</span></span>

## <span data-ttu-id="325a6-131">筆記</span><span class="sxs-lookup"><span data-stu-id="325a6-131">NOTES</span></span>

## <span data-ttu-id="325a6-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="325a6-132">RELATED LINKS</span></span>
