---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 746033cfdf48782d10c0fdabf7a018d309269afb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443707"
---
# <span data-ttu-id="97a68-101">Remove-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="97a68-101">Remove-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="97a68-102">摘要</span><span class="sxs-lookup"><span data-stu-id="97a68-102">SYNOPSIS</span></span>
<span data-ttu-id="97a68-103">從指定的 HybridConnection 命名空間中移除 HybridConnection。</span><span class="sxs-lookup"><span data-stu-id="97a68-103">Removes the HybridConnection from the specified HybridConnection namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97a68-104">句法</span><span class="sxs-lookup"><span data-stu-id="97a68-104">SYNTAX</span></span>

```
Remove-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97a68-105">說明</span><span class="sxs-lookup"><span data-stu-id="97a68-105">DESCRIPTION</span></span>
<span data-ttu-id="97a68-106">**AzureRmRelayHybridConnection** Cmdlet 會從指定的中繼命名空間中移除 HybridConnection。</span><span class="sxs-lookup"><span data-stu-id="97a68-106">The **Remove-AzureRmRelayHybridConnection** cmdlet removes the HybridConnection from the specified Relay namespace.</span></span>

## <span data-ttu-id="97a68-107">示例</span><span class="sxs-lookup"><span data-stu-id="97a68-107">EXAMPLES</span></span>

### <span data-ttu-id="97a68-108">範例1</span><span class="sxs-lookup"><span data-stu-id="97a68-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="97a68-109">`TestHybridConnection`從命名空間中移除 HybridConnection `TestNameSpace-Relay1` 。</span><span class="sxs-lookup"><span data-stu-id="97a68-109">Removes the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="97a68-110">參數</span><span class="sxs-lookup"><span data-stu-id="97a68-110">PARAMETERS</span></span>

### <span data-ttu-id="97a68-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97a68-111">-DefaultProfile</span></span>
<span data-ttu-id="97a68-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="97a68-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97a68-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="97a68-113">-Name</span></span>
<span data-ttu-id="97a68-114">HybridConnections [名稱]。</span><span class="sxs-lookup"><span data-stu-id="97a68-114">HybridConnections Name.</span></span>

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

### <span data-ttu-id="97a68-115">-命名空間</span><span class="sxs-lookup"><span data-stu-id="97a68-115">-Namespace</span></span>
<span data-ttu-id="97a68-116">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="97a68-116">Namespace Name.</span></span>

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

### <span data-ttu-id="97a68-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97a68-117">-ResourceGroupName</span></span>
<span data-ttu-id="97a68-118">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="97a68-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="97a68-119">-確認</span><span class="sxs-lookup"><span data-stu-id="97a68-119">-Confirm</span></span>
<span data-ttu-id="97a68-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="97a68-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97a68-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97a68-121">-WhatIf</span></span>
<span data-ttu-id="97a68-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="97a68-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97a68-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="97a68-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97a68-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97a68-124">CommonParameters</span></span>
<span data-ttu-id="97a68-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="97a68-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="97a68-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="97a68-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97a68-127">輸入</span><span class="sxs-lookup"><span data-stu-id="97a68-127">INPUTS</span></span>

### <span data-ttu-id="97a68-128">System.object</span><span class="sxs-lookup"><span data-stu-id="97a68-128">System.String</span></span>


## <span data-ttu-id="97a68-129">輸出</span><span class="sxs-lookup"><span data-stu-id="97a68-129">OUTPUTS</span></span>

### <span data-ttu-id="97a68-130">System.void</span><span class="sxs-lookup"><span data-stu-id="97a68-130">System.Void</span></span>


## <span data-ttu-id="97a68-131">筆記</span><span class="sxs-lookup"><span data-stu-id="97a68-131">NOTES</span></span>

## <span data-ttu-id="97a68-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="97a68-132">RELATED LINKS</span></span>
