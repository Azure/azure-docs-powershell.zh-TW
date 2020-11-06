---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
ms.openlocfilehash: 56f0c3ec3a69819ad7faa28b10d33a3cf751c48f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448105"
---
# <span data-ttu-id="1f512-101">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1f512-101">Set-AzureRmRouteFilter</span></span>

## <span data-ttu-id="1f512-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1f512-102">SYNOPSIS</span></span>
<span data-ttu-id="1f512-103">{{填入摘要}}</span><span class="sxs-lookup"><span data-stu-id="1f512-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f512-104">句法</span><span class="sxs-lookup"><span data-stu-id="1f512-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f512-105">說明</span><span class="sxs-lookup"><span data-stu-id="1f512-105">DESCRIPTION</span></span>
<span data-ttu-id="1f512-106">{{填入描述}}</span><span class="sxs-lookup"><span data-stu-id="1f512-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="1f512-107">示例</span><span class="sxs-lookup"><span data-stu-id="1f512-107">EXAMPLES</span></span>

### <span data-ttu-id="1f512-108">範例1</span><span class="sxs-lookup"><span data-stu-id="1f512-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="1f512-109">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="1f512-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="1f512-110">參數</span><span class="sxs-lookup"><span data-stu-id="1f512-110">PARAMETERS</span></span>

### <span data-ttu-id="1f512-111">-Force</span><span class="sxs-lookup"><span data-stu-id="1f512-111">-Force</span></span>
<span data-ttu-id="1f512-112">如果您想要 overrite 資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="1f512-112">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f512-113">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="1f512-113">-RouteFilter</span></span>
<span data-ttu-id="1f512-114">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="1f512-114">The RouteFilter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f512-115">-確認</span><span class="sxs-lookup"><span data-stu-id="1f512-115">-Confirm</span></span>
<span data-ttu-id="1f512-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1f512-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f512-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f512-117">-WhatIf</span></span>
<span data-ttu-id="1f512-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1f512-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f512-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1f512-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f512-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f512-120">-DefaultProfile</span></span>
<span data-ttu-id="1f512-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1f512-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f512-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f512-122">CommonParameters</span></span>
<span data-ttu-id="1f512-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1f512-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f512-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1f512-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f512-125">輸入</span><span class="sxs-lookup"><span data-stu-id="1f512-125">INPUTS</span></span>

### <span data-ttu-id="1f512-126">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1f512-126">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="1f512-127">輸出</span><span class="sxs-lookup"><span data-stu-id="1f512-127">OUTPUTS</span></span>

### <span data-ttu-id="1f512-128">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1f512-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="1f512-129">筆記</span><span class="sxs-lookup"><span data-stu-id="1f512-129">NOTES</span></span>

## <span data-ttu-id="1f512-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="1f512-130">RELATED LINKS</span></span>

