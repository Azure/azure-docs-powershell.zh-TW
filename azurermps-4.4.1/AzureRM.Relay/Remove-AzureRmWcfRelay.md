---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmWcfRelay.md
ms.openlocfilehash: a774f388690ab2ee0528e94a2a96addecf1687fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456423"
---
# <span data-ttu-id="9b385-101">Remove-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="9b385-101">Remove-AzureRmWcfRelay</span></span>

## <span data-ttu-id="9b385-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9b385-102">SYNOPSIS</span></span>
<span data-ttu-id="9b385-103">從指定的中繼命名空間中移除 WcfRelay。</span><span class="sxs-lookup"><span data-stu-id="9b385-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b385-104">句法</span><span class="sxs-lookup"><span data-stu-id="9b385-104">SYNTAX</span></span>

```
Remove-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b385-105">說明</span><span class="sxs-lookup"><span data-stu-id="9b385-105">DESCRIPTION</span></span>
<span data-ttu-id="9b385-106">**AzureRmWcfRelay** Cmdlet 會從指定的中繼命名空間中移除 WcfRelay。</span><span class="sxs-lookup"><span data-stu-id="9b385-106">The **Remove-AzureRmWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="9b385-107">示例</span><span class="sxs-lookup"><span data-stu-id="9b385-107">EXAMPLES</span></span>

### <span data-ttu-id="9b385-108">範例1</span><span class="sxs-lookup"><span data-stu-id="9b385-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="9b385-109">`TestWCFRelay1`從命名空間中移除 WcfRelay `TestNameSpace-Relay1` 。</span><span class="sxs-lookup"><span data-stu-id="9b385-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="9b385-110">參數</span><span class="sxs-lookup"><span data-stu-id="9b385-110">PARAMETERS</span></span>

### <span data-ttu-id="9b385-111">-命名空間</span><span class="sxs-lookup"><span data-stu-id="9b385-111">-Namespace</span></span>
<span data-ttu-id="9b385-112">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="9b385-112">Namespace Name.</span></span>

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

### <span data-ttu-id="9b385-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b385-113">-ResourceGroupName</span></span>
<span data-ttu-id="9b385-114">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="9b385-114">Resource Group Name.</span></span>

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

### <span data-ttu-id="9b385-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="9b385-115">-Name</span></span>
<span data-ttu-id="9b385-116">WcfRelay [名稱]。</span><span class="sxs-lookup"><span data-stu-id="9b385-116">WcfRelay Name.</span></span>

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

### <span data-ttu-id="9b385-117">-確認</span><span class="sxs-lookup"><span data-stu-id="9b385-117">-Confirm</span></span>
<span data-ttu-id="9b385-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9b385-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b385-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b385-119">-WhatIf</span></span>
<span data-ttu-id="9b385-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9b385-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b385-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9b385-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b385-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b385-122">-DefaultProfile</span></span>
<span data-ttu-id="9b385-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9b385-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b385-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b385-124">CommonParameters</span></span>
<span data-ttu-id="9b385-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9b385-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b385-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9b385-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b385-127">輸入</span><span class="sxs-lookup"><span data-stu-id="9b385-127">INPUTS</span></span>

### <span data-ttu-id="9b385-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b385-128">-ResourceGroupName</span></span>
 <span data-ttu-id="9b385-129">System.object</span><span class="sxs-lookup"><span data-stu-id="9b385-129">System.String</span></span>
 

### <span data-ttu-id="9b385-130">-命名空間</span><span class="sxs-lookup"><span data-stu-id="9b385-130">-Namespace</span></span>
 <span data-ttu-id="9b385-131">System.object</span><span class="sxs-lookup"><span data-stu-id="9b385-131">System.String</span></span>
 

### <span data-ttu-id="9b385-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="9b385-132">-Name</span></span>
 <span data-ttu-id="9b385-133">System.object</span><span class="sxs-lookup"><span data-stu-id="9b385-133">System.String</span></span>

## <span data-ttu-id="9b385-134">輸出</span><span class="sxs-lookup"><span data-stu-id="9b385-134">OUTPUTS</span></span>

### <span data-ttu-id="9b385-135">System.object</span><span class="sxs-lookup"><span data-stu-id="9b385-135">System.Object</span></span>

## <span data-ttu-id="9b385-136">筆記</span><span class="sxs-lookup"><span data-stu-id="9b385-136">NOTES</span></span>

## <span data-ttu-id="9b385-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="9b385-137">RELATED LINKS</span></span>

