---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermroutefilter
schema: 2.0.0
ms.openlocfilehash: 3622b7ad87658091d4b54af62678d12a324ef56a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802270"
---
# <span data-ttu-id="f9125-101">Remove-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f9125-101">Remove-AzureRmRouteFilter</span></span>

## <span data-ttu-id="f9125-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f9125-102">SYNOPSIS</span></span>
<span data-ttu-id="f9125-103">{{填入摘要}}</span><span class="sxs-lookup"><span data-stu-id="f9125-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9125-104">句法</span><span class="sxs-lookup"><span data-stu-id="f9125-104">SYNTAX</span></span>

```
Remove-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9125-105">說明</span><span class="sxs-lookup"><span data-stu-id="f9125-105">DESCRIPTION</span></span>
<span data-ttu-id="f9125-106">{{填入描述}}</span><span class="sxs-lookup"><span data-stu-id="f9125-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="f9125-107">示例</span><span class="sxs-lookup"><span data-stu-id="f9125-107">EXAMPLES</span></span>

### <span data-ttu-id="f9125-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f9125-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="f9125-109">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="f9125-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="f9125-110">參數</span><span class="sxs-lookup"><span data-stu-id="f9125-110">PARAMETERS</span></span>

### <span data-ttu-id="f9125-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9125-111">-DefaultProfile</span></span>
<span data-ttu-id="f9125-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f9125-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9125-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f9125-113">-Force</span></span>
<span data-ttu-id="f9125-114">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="f9125-114">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9125-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="f9125-115">-Name</span></span>
<span data-ttu-id="f9125-116">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="f9125-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9125-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f9125-117">-PassThru</span></span>
<span data-ttu-id="f9125-118">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="f9125-118">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9125-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9125-119">-ResourceGroupName</span></span>
<span data-ttu-id="f9125-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f9125-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9125-121">-確認</span><span class="sxs-lookup"><span data-stu-id="f9125-121">-Confirm</span></span>
<span data-ttu-id="f9125-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f9125-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9125-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9125-123">-WhatIf</span></span>
<span data-ttu-id="f9125-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f9125-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9125-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f9125-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9125-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9125-126">CommonParameters</span></span>
<span data-ttu-id="f9125-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f9125-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9125-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f9125-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9125-129">輸入</span><span class="sxs-lookup"><span data-stu-id="f9125-129">INPUTS</span></span>

### <span data-ttu-id="f9125-130">System.object</span><span class="sxs-lookup"><span data-stu-id="f9125-130">System.String</span></span>

## <span data-ttu-id="f9125-131">輸出</span><span class="sxs-lookup"><span data-stu-id="f9125-131">OUTPUTS</span></span>

### <span data-ttu-id="f9125-132">System.object</span><span class="sxs-lookup"><span data-stu-id="f9125-132">System.Object</span></span>

## <span data-ttu-id="f9125-133">筆記</span><span class="sxs-lookup"><span data-stu-id="f9125-133">NOTES</span></span>

## <span data-ttu-id="f9125-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="f9125-134">RELATED LINKS</span></span>

