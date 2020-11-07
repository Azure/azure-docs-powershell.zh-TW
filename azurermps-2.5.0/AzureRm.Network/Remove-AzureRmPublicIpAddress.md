---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermpublicipaddress
schema: 2.0.0
ms.openlocfilehash: af8a85c698a59a31516c6dee05bb57415a45ff62
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800753"
---
# <span data-ttu-id="c998f-101">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c998f-101">Remove-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="c998f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c998f-102">SYNOPSIS</span></span>
<span data-ttu-id="c998f-103">移除公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c998f-103">Removes a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c998f-104">句法</span><span class="sxs-lookup"><span data-stu-id="c998f-104">SYNTAX</span></span>

```
Remove-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c998f-105">說明</span><span class="sxs-lookup"><span data-stu-id="c998f-105">DESCRIPTION</span></span>
<span data-ttu-id="c998f-106">**AzureRmPublicIpAddress** Cmdlet 會移除 AZURE 公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c998f-106">The **Remove-AzureRmPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="c998f-107">示例</span><span class="sxs-lookup"><span data-stu-id="c998f-107">EXAMPLES</span></span>

### <span data-ttu-id="c998f-108">1：移除公用 IP 位址資源</span><span class="sxs-lookup"><span data-stu-id="c998f-108">1: Remove a public IP address resource</span></span>
```
Remove-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="c998f-109">這個命令會移除 [資源] 群組 $rgName 中名為 $publicIpName 的公用 IP 位址資源。</span><span class="sxs-lookup"><span data-stu-id="c998f-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="c998f-110">參數</span><span class="sxs-lookup"><span data-stu-id="c998f-110">PARAMETERS</span></span>

### <span data-ttu-id="c998f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c998f-111">-AsJob</span></span>
<span data-ttu-id="c998f-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c998f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c998f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c998f-113">-DefaultProfile</span></span>
<span data-ttu-id="c998f-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c998f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c998f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c998f-115">-Force</span></span>
<span data-ttu-id="c998f-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="c998f-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c998f-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="c998f-117">-Name</span></span>
<span data-ttu-id="c998f-118">指定此 Cmdlet 移除之公用 IP 位址的名稱。</span><span class="sxs-lookup"><span data-stu-id="c998f-118">Specifies the name of the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c998f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c998f-119">-PassThru</span></span>
<span data-ttu-id="c998f-120">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="c998f-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c998f-121">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="c998f-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c998f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c998f-122">-ResourceGroupName</span></span>
<span data-ttu-id="c998f-123">指定包含此 Cmdlet 移除之公用 IP 位址之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c998f-123">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c998f-124">-確認</span><span class="sxs-lookup"><span data-stu-id="c998f-124">-Confirm</span></span>
<span data-ttu-id="c998f-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c998f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c998f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c998f-126">-WhatIf</span></span>
<span data-ttu-id="c998f-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c998f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c998f-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c998f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c998f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c998f-129">CommonParameters</span></span>
<span data-ttu-id="c998f-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c998f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c998f-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c998f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c998f-132">輸入</span><span class="sxs-lookup"><span data-stu-id="c998f-132">INPUTS</span></span>

## <span data-ttu-id="c998f-133">輸出</span><span class="sxs-lookup"><span data-stu-id="c998f-133">OUTPUTS</span></span>

## <span data-ttu-id="c998f-134">筆記</span><span class="sxs-lookup"><span data-stu-id="c998f-134">NOTES</span></span>

## <span data-ttu-id="c998f-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="c998f-135">RELATED LINKS</span></span>

[<span data-ttu-id="c998f-136">AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c998f-136">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="c998f-137">新-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c998f-137">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="c998f-138">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c998f-138">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


