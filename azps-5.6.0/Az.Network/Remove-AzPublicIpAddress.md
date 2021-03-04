---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpAddress.md
ms.openlocfilehash: f8a509fc73387361de5bd191ee9eefc61c33a5f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913374"
---
# <span data-ttu-id="ad504-101">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ad504-101">Remove-AzPublicIpAddress</span></span>

## <span data-ttu-id="ad504-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ad504-102">SYNOPSIS</span></span>
<span data-ttu-id="ad504-103">移除公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ad504-103">Removes a public IP address.</span></span>

## <span data-ttu-id="ad504-104">語法</span><span class="sxs-lookup"><span data-stu-id="ad504-104">SYNTAX</span></span>

```
Remove-AzPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad504-105">描述</span><span class="sxs-lookup"><span data-stu-id="ad504-105">DESCRIPTION</span></span>
<span data-ttu-id="ad504-106">**Remove-AzPublicIpAddress** Cmdlet 會移除 Azure 公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ad504-106">The **Remove-AzPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="ad504-107">例子</span><span class="sxs-lookup"><span data-stu-id="ad504-107">EXAMPLES</span></span>

### <span data-ttu-id="ad504-108">1：移除公用 IP 位址資源</span><span class="sxs-lookup"><span data-stu-id="ad504-108">1: Remove a public IP address resource</span></span>
```
Remove-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="ad504-109">此命令會移除資源群組中名為 $publicIpName 的公用 IP 位址$rgName。</span><span class="sxs-lookup"><span data-stu-id="ad504-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="ad504-110">參數</span><span class="sxs-lookup"><span data-stu-id="ad504-110">PARAMETERS</span></span>

### <span data-ttu-id="ad504-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad504-111">-AsJob</span></span>
<span data-ttu-id="ad504-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad504-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ad504-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad504-113">-DefaultProfile</span></span>
<span data-ttu-id="ad504-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ad504-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad504-115">-強制</span><span class="sxs-lookup"><span data-stu-id="ad504-115">-Force</span></span>
<span data-ttu-id="ad504-116">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="ad504-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ad504-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="ad504-117">-Name</span></span>
<span data-ttu-id="ad504-118">指定此 Cmdlet 移除的公用 IP 位址名稱。</span><span class="sxs-lookup"><span data-stu-id="ad504-118">Specifies the name of the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ad504-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad504-119">-PassThru</span></span>
<span data-ttu-id="ad504-120">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="ad504-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ad504-121">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="ad504-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ad504-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad504-122">-ResourceGroupName</span></span>
<span data-ttu-id="ad504-123">指定包含此 Cmdlet 移除之公用 IP 位址的資源組名。</span><span class="sxs-lookup"><span data-stu-id="ad504-123">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ad504-124">-確認</span><span class="sxs-lookup"><span data-stu-id="ad504-124">-Confirm</span></span>
<span data-ttu-id="ad504-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ad504-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad504-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad504-126">-WhatIf</span></span>
<span data-ttu-id="ad504-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ad504-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad504-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad504-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad504-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad504-129">CommonParameters</span></span>
<span data-ttu-id="ad504-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ad504-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad504-131">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ad504-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad504-132">輸入</span><span class="sxs-lookup"><span data-stu-id="ad504-132">INPUTS</span></span>

### <span data-ttu-id="ad504-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ad504-133">System.String</span></span>

## <span data-ttu-id="ad504-134">輸出</span><span class="sxs-lookup"><span data-stu-id="ad504-134">OUTPUTS</span></span>

### <span data-ttu-id="ad504-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ad504-135">System.Boolean</span></span>

## <span data-ttu-id="ad504-136">筆記</span><span class="sxs-lookup"><span data-stu-id="ad504-136">NOTES</span></span>

## <span data-ttu-id="ad504-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="ad504-137">RELATED LINKS</span></span>

[<span data-ttu-id="ad504-138">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ad504-138">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="ad504-139">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ad504-139">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="ad504-140">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ad504-140">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


