---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
ms.openlocfilehash: 463ef6d1d23ffe809d8810a9cbf4dd0ebf1ff578
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100138015"
---
# <span data-ttu-id="f7f83-101">Remove-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="f7f83-101">Remove-AzRelayNamespace</span></span>

## <span data-ttu-id="f7f83-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f7f83-102">SYNOPSIS</span></span>
<span data-ttu-id="f7f83-103">從指定的資源群組中移除命名空間。</span><span class="sxs-lookup"><span data-stu-id="f7f83-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="f7f83-104">句法</span><span class="sxs-lookup"><span data-stu-id="f7f83-104">SYNTAX</span></span>

```
Remove-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7f83-105">說明</span><span class="sxs-lookup"><span data-stu-id="f7f83-105">DESCRIPTION</span></span>
<span data-ttu-id="f7f83-106">**AzRelayNamespace** Cmdlet 會從指定的資源群組中移除命名空間。</span><span class="sxs-lookup"><span data-stu-id="f7f83-106">The **Remove-AzRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="f7f83-107">示例</span><span class="sxs-lookup"><span data-stu-id="f7f83-107">EXAMPLES</span></span>

### <span data-ttu-id="f7f83-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f7f83-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="f7f83-109">`TestNameSpace-Relay1`從指定的資源群組中移除中繼命名空間 `Default-ServiceBus-WestUS` 。</span><span class="sxs-lookup"><span data-stu-id="f7f83-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="f7f83-110">參數</span><span class="sxs-lookup"><span data-stu-id="f7f83-110">PARAMETERS</span></span>

### <span data-ttu-id="f7f83-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7f83-111">-DefaultProfile</span></span>
<span data-ttu-id="f7f83-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f7f83-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7f83-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="f7f83-113">-Name</span></span>
<span data-ttu-id="f7f83-114">中繼命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="f7f83-114">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="f7f83-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7f83-115">-ResourceGroupName</span></span>
<span data-ttu-id="f7f83-116">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="f7f83-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="f7f83-117">-確認</span><span class="sxs-lookup"><span data-stu-id="f7f83-117">-Confirm</span></span>
<span data-ttu-id="f7f83-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f7f83-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7f83-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7f83-119">-WhatIf</span></span>
<span data-ttu-id="f7f83-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f7f83-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7f83-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f7f83-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7f83-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7f83-122">CommonParameters</span></span>
<span data-ttu-id="f7f83-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f7f83-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7f83-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f7f83-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7f83-125">輸入</span><span class="sxs-lookup"><span data-stu-id="f7f83-125">INPUTS</span></span>

### <span data-ttu-id="f7f83-126">System.object</span><span class="sxs-lookup"><span data-stu-id="f7f83-126">System.String</span></span>

## <span data-ttu-id="f7f83-127">輸出</span><span class="sxs-lookup"><span data-stu-id="f7f83-127">OUTPUTS</span></span>

### <span data-ttu-id="f7f83-128">System.void</span><span class="sxs-lookup"><span data-stu-id="f7f83-128">System.Void</span></span>

## <span data-ttu-id="f7f83-129">筆記</span><span class="sxs-lookup"><span data-stu-id="f7f83-129">NOTES</span></span>

## <span data-ttu-id="f7f83-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7f83-130">RELATED LINKS</span></span>
