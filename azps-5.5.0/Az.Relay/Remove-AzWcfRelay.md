---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
ms.openlocfilehash: 238c4ecf92cbdd1dc6e9e0a430ec8e6ad200b967
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139987"
---
# <span data-ttu-id="4cec1-101">Remove-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="4cec1-101">Remove-AzWcfRelay</span></span>

## <span data-ttu-id="4cec1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4cec1-102">SYNOPSIS</span></span>
<span data-ttu-id="4cec1-103">從指定的中繼命名空間中移除 WcfRelay。</span><span class="sxs-lookup"><span data-stu-id="4cec1-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="4cec1-104">句法</span><span class="sxs-lookup"><span data-stu-id="4cec1-104">SYNTAX</span></span>

```
Remove-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cec1-105">說明</span><span class="sxs-lookup"><span data-stu-id="4cec1-105">DESCRIPTION</span></span>
<span data-ttu-id="4cec1-106">**AzWcfRelay** Cmdlet 會從指定的中繼命名空間中移除 WcfRelay。</span><span class="sxs-lookup"><span data-stu-id="4cec1-106">The **Remove-AzWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="4cec1-107">示例</span><span class="sxs-lookup"><span data-stu-id="4cec1-107">EXAMPLES</span></span>

### <span data-ttu-id="4cec1-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4cec1-108">Example 1</span></span>
```
PS C:\> Remove-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="4cec1-109">`TestWCFRelay1`從命名空間中移除 WcfRelay `TestNameSpace-Relay1` 。</span><span class="sxs-lookup"><span data-stu-id="4cec1-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="4cec1-110">參數</span><span class="sxs-lookup"><span data-stu-id="4cec1-110">PARAMETERS</span></span>

### <span data-ttu-id="4cec1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cec1-111">-DefaultProfile</span></span>
<span data-ttu-id="4cec1-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4cec1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cec1-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="4cec1-113">-Name</span></span>
<span data-ttu-id="4cec1-114">WcfRelay [名稱]。</span><span class="sxs-lookup"><span data-stu-id="4cec1-114">WcfRelay Name.</span></span>

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

### <span data-ttu-id="4cec1-115">-命名空間</span><span class="sxs-lookup"><span data-stu-id="4cec1-115">-Namespace</span></span>
<span data-ttu-id="4cec1-116">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="4cec1-116">Namespace Name.</span></span>

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

### <span data-ttu-id="4cec1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cec1-117">-ResourceGroupName</span></span>
<span data-ttu-id="4cec1-118">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="4cec1-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="4cec1-119">-確認</span><span class="sxs-lookup"><span data-stu-id="4cec1-119">-Confirm</span></span>
<span data-ttu-id="4cec1-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4cec1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cec1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cec1-121">-WhatIf</span></span>
<span data-ttu-id="4cec1-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4cec1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cec1-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4cec1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cec1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cec1-124">CommonParameters</span></span>
<span data-ttu-id="4cec1-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4cec1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cec1-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4cec1-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cec1-127">輸入</span><span class="sxs-lookup"><span data-stu-id="4cec1-127">INPUTS</span></span>

### <span data-ttu-id="4cec1-128">System.object</span><span class="sxs-lookup"><span data-stu-id="4cec1-128">System.String</span></span>

## <span data-ttu-id="4cec1-129">輸出</span><span class="sxs-lookup"><span data-stu-id="4cec1-129">OUTPUTS</span></span>

### <span data-ttu-id="4cec1-130">System.void</span><span class="sxs-lookup"><span data-stu-id="4cec1-130">System.Void</span></span>

## <span data-ttu-id="4cec1-131">筆記</span><span class="sxs-lookup"><span data-stu-id="4cec1-131">NOTES</span></span>

## <span data-ttu-id="4cec1-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="4cec1-132">RELATED LINKS</span></span>
