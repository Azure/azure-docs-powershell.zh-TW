---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayNamespace.md
ms.openlocfilehash: 52abd413f94d0c190a6f03b3707efdb544a4b72a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447694"
---
# <span data-ttu-id="9d835-101">Remove-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="9d835-101">Remove-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="9d835-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9d835-102">SYNOPSIS</span></span>
<span data-ttu-id="9d835-103">從指定的資源群組中移除命名空間。</span><span class="sxs-lookup"><span data-stu-id="9d835-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d835-104">句法</span><span class="sxs-lookup"><span data-stu-id="9d835-104">SYNTAX</span></span>

```
Remove-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d835-105">說明</span><span class="sxs-lookup"><span data-stu-id="9d835-105">DESCRIPTION</span></span>
<span data-ttu-id="9d835-106">**AzureRmRelayNamespace** Cmdlet 會從指定的資源群組中移除命名空間。</span><span class="sxs-lookup"><span data-stu-id="9d835-106">The **Remove-AzureRmRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="9d835-107">示例</span><span class="sxs-lookup"><span data-stu-id="9d835-107">EXAMPLES</span></span>

### <span data-ttu-id="9d835-108">範例1</span><span class="sxs-lookup"><span data-stu-id="9d835-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="9d835-109">`TestNameSpace-Relay1`從指定的資源群組中移除中繼命名空間 `Default-ServiceBus-WestUS` 。</span><span class="sxs-lookup"><span data-stu-id="9d835-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="9d835-110">參數</span><span class="sxs-lookup"><span data-stu-id="9d835-110">PARAMETERS</span></span>

### <span data-ttu-id="9d835-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d835-111">-DefaultProfile</span></span>
<span data-ttu-id="9d835-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9d835-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d835-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="9d835-113">-Name</span></span>
<span data-ttu-id="9d835-114">中繼命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="9d835-114">Relay Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d835-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d835-115">-ResourceGroupName</span></span>
<span data-ttu-id="9d835-116">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="9d835-116">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d835-117">-確認</span><span class="sxs-lookup"><span data-stu-id="9d835-117">-Confirm</span></span>
<span data-ttu-id="9d835-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9d835-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d835-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d835-119">-WhatIf</span></span>
<span data-ttu-id="9d835-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9d835-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d835-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9d835-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d835-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d835-122">CommonParameters</span></span>
<span data-ttu-id="9d835-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9d835-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d835-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9d835-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d835-125">輸入</span><span class="sxs-lookup"><span data-stu-id="9d835-125">INPUTS</span></span>

### <span data-ttu-id="9d835-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d835-126">-ResourceGroupName</span></span>
 <span data-ttu-id="9d835-127">System.object</span><span class="sxs-lookup"><span data-stu-id="9d835-127">System.String</span></span>

### <span data-ttu-id="9d835-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="9d835-128">-Name</span></span>
 <span data-ttu-id="9d835-129">System.object</span><span class="sxs-lookup"><span data-stu-id="9d835-129">System.String</span></span>

## <span data-ttu-id="9d835-130">輸出</span><span class="sxs-lookup"><span data-stu-id="9d835-130">OUTPUTS</span></span>

### <span data-ttu-id="9d835-131">System.object</span><span class="sxs-lookup"><span data-stu-id="9d835-131">System.Object</span></span>

## <span data-ttu-id="9d835-132">筆記</span><span class="sxs-lookup"><span data-stu-id="9d835-132">NOTES</span></span>

## <span data-ttu-id="9d835-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="9d835-133">RELATED LINKS</span></span>

