---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancer.md
ms.openlocfilehash: 6757c9c0b9eeb0b3408a07713c62812d361d814a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456476"
---
# <span data-ttu-id="b881a-101">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b881a-101">Remove-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="b881a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b881a-102">SYNOPSIS</span></span>
<span data-ttu-id="b881a-103">移除負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="b881a-103">Removes a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b881a-104">句法</span><span class="sxs-lookup"><span data-stu-id="b881a-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancer -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b881a-105">說明</span><span class="sxs-lookup"><span data-stu-id="b881a-105">DESCRIPTION</span></span>
<span data-ttu-id="b881a-106">**AzureRmLoadBalancer** Cmdlet 會移除 Azure 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="b881a-106">The **Remove-AzureRmLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="b881a-107">示例</span><span class="sxs-lookup"><span data-stu-id="b881a-107">EXAMPLES</span></span>

### <span data-ttu-id="b881a-108">範例1：移除負載平衡器</span><span class="sxs-lookup"><span data-stu-id="b881a-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="b881a-109">這個命令會刪除名為 MyResourceGroup 的資源群組中名為 MyLoadBalancer 的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="b881a-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="b881a-110">參數</span><span class="sxs-lookup"><span data-stu-id="b881a-110">PARAMETERS</span></span>

### <span data-ttu-id="b881a-111">-Force</span><span class="sxs-lookup"><span data-stu-id="b881a-111">-Force</span></span>
<span data-ttu-id="b881a-112">指示此 Cmdlet 會移除負載平衡器，不論是否已將資源指派給它。</span><span class="sxs-lookup"><span data-stu-id="b881a-112">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b881a-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="b881a-113">-Name</span></span>
<span data-ttu-id="b881a-114">指定要移除的負載平衡器的名稱。</span><span class="sxs-lookup"><span data-stu-id="b881a-114">Specifies the name of the load balancer to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b881a-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b881a-115">-PassThru</span></span>
<span data-ttu-id="b881a-116">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="b881a-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b881a-117">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="b881a-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b881a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b881a-118">-ResourceGroupName</span></span>
<span data-ttu-id="b881a-119">指定包含要移除之負載等化器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b881a-119">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b881a-120">-確認</span><span class="sxs-lookup"><span data-stu-id="b881a-120">-Confirm</span></span>
<span data-ttu-id="b881a-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b881a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b881a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b881a-122">-WhatIf</span></span>
<span data-ttu-id="b881a-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b881a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b881a-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b881a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b881a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b881a-125">-DefaultProfile</span></span>
<span data-ttu-id="b881a-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b881a-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b881a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b881a-127">CommonParameters</span></span>
<span data-ttu-id="b881a-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b881a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b881a-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b881a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b881a-130">輸入</span><span class="sxs-lookup"><span data-stu-id="b881a-130">INPUTS</span></span>

## <span data-ttu-id="b881a-131">輸出</span><span class="sxs-lookup"><span data-stu-id="b881a-131">OUTPUTS</span></span>

## <span data-ttu-id="b881a-132">筆記</span><span class="sxs-lookup"><span data-stu-id="b881a-132">NOTES</span></span>

## <span data-ttu-id="b881a-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="b881a-133">RELATED LINKS</span></span>

[<span data-ttu-id="b881a-134">AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b881a-134">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="b881a-135">新-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b881a-135">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="b881a-136">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b881a-136">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)


