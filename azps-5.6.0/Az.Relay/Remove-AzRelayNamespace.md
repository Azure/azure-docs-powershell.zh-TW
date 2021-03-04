---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/remove-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
ms.openlocfilehash: 17a5cb5c05b9bd3293b15ef48b90c8d7387744da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914569"
---
# <span data-ttu-id="b34c2-101">Remove-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="b34c2-101">Remove-AzRelayNamespace</span></span>

## <span data-ttu-id="b34c2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b34c2-102">SYNOPSIS</span></span>
<span data-ttu-id="b34c2-103">從指定的資源群組移除命名空間。</span><span class="sxs-lookup"><span data-stu-id="b34c2-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="b34c2-104">語法</span><span class="sxs-lookup"><span data-stu-id="b34c2-104">SYNTAX</span></span>

```
Remove-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b34c2-105">描述</span><span class="sxs-lookup"><span data-stu-id="b34c2-105">DESCRIPTION</span></span>
<span data-ttu-id="b34c2-106">**Remove-AzRelayNamespace** Cmdlet 會從指定的資源群組移除命名空間。</span><span class="sxs-lookup"><span data-stu-id="b34c2-106">The **Remove-AzRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="b34c2-107">例子</span><span class="sxs-lookup"><span data-stu-id="b34c2-107">EXAMPLES</span></span>

### <span data-ttu-id="b34c2-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="b34c2-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="b34c2-109">從指定的資源群組移除 Relay `TestNameSpace-Relay1` 命名空間 `Default-ServiceBus-WestUS` 。</span><span class="sxs-lookup"><span data-stu-id="b34c2-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="b34c2-110">參數</span><span class="sxs-lookup"><span data-stu-id="b34c2-110">PARAMETERS</span></span>

### <span data-ttu-id="b34c2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b34c2-111">-DefaultProfile</span></span>
<span data-ttu-id="b34c2-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b34c2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b34c2-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="b34c2-113">-Name</span></span>
<span data-ttu-id="b34c2-114">轉場命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="b34c2-114">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="b34c2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b34c2-115">-ResourceGroupName</span></span>
<span data-ttu-id="b34c2-116">資源組名。</span><span class="sxs-lookup"><span data-stu-id="b34c2-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="b34c2-117">-確認</span><span class="sxs-lookup"><span data-stu-id="b34c2-117">-Confirm</span></span>
<span data-ttu-id="b34c2-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b34c2-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b34c2-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b34c2-119">-WhatIf</span></span>
<span data-ttu-id="b34c2-120">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b34c2-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b34c2-121">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b34c2-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b34c2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b34c2-122">CommonParameters</span></span>
<span data-ttu-id="b34c2-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b34c2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b34c2-124">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b34c2-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b34c2-125">輸入</span><span class="sxs-lookup"><span data-stu-id="b34c2-125">INPUTS</span></span>

### <span data-ttu-id="b34c2-126">System.String</span><span class="sxs-lookup"><span data-stu-id="b34c2-126">System.String</span></span>

## <span data-ttu-id="b34c2-127">輸出</span><span class="sxs-lookup"><span data-stu-id="b34c2-127">OUTPUTS</span></span>

### <span data-ttu-id="b34c2-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="b34c2-128">System.Void</span></span>

## <span data-ttu-id="b34c2-129">筆記</span><span class="sxs-lookup"><span data-stu-id="b34c2-129">NOTES</span></span>

## <span data-ttu-id="b34c2-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="b34c2-130">RELATED LINKS</span></span>
