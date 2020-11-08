---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpAddress.md
ms.openlocfilehash: 8d3c71d1cf4df9483f379d8a689597a1a10c7ce7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139687"
---
# <span data-ttu-id="7cbf8-101">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7cbf8-101">Remove-AzPublicIpAddress</span></span>

## <span data-ttu-id="7cbf8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7cbf8-102">SYNOPSIS</span></span>
<span data-ttu-id="7cbf8-103">移除公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="7cbf8-103">Removes a public IP address.</span></span>

## <span data-ttu-id="7cbf8-104">句法</span><span class="sxs-lookup"><span data-stu-id="7cbf8-104">SYNTAX</span></span>

```
Remove-AzPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cbf8-105">說明</span><span class="sxs-lookup"><span data-stu-id="7cbf8-105">DESCRIPTION</span></span>
<span data-ttu-id="7cbf8-106">**AzPublicIpAddress** Cmdlet 會移除 AZURE 公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="7cbf8-106">The **Remove-AzPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="7cbf8-107">示例</span><span class="sxs-lookup"><span data-stu-id="7cbf8-107">EXAMPLES</span></span>

### <span data-ttu-id="7cbf8-108">1：移除公用 IP 位址資源</span><span class="sxs-lookup"><span data-stu-id="7cbf8-108">1: Remove a public IP address resource</span></span>
```
Remove-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="7cbf8-109">這個命令會移除 [資源] 群組 $rgName 中名為 $publicIpName 的公用 IP 位址資源。</span><span class="sxs-lookup"><span data-stu-id="7cbf8-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="7cbf8-110">參數</span><span class="sxs-lookup"><span data-stu-id="7cbf8-110">PARAMETERS</span></span>

### <span data-ttu-id="7cbf8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7cbf8-111">-AsJob</span></span>
<span data-ttu-id="7cbf8-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7cbf8-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7cbf8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cbf8-113">-DefaultProfile</span></span>
<span data-ttu-id="7cbf8-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7cbf8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cbf8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7cbf8-115">-Force</span></span>
<span data-ttu-id="7cbf8-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="7cbf8-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7cbf8-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="7cbf8-117">-Name</span></span>
<span data-ttu-id="7cbf8-118">指定此 Cmdlet 移除之公用 IP 位址的名稱。</span><span class="sxs-lookup"><span data-stu-id="7cbf8-118">Specifies the name of the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7cbf8-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7cbf8-119">-PassThru</span></span>
<span data-ttu-id="7cbf8-120">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="7cbf8-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7cbf8-121">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="7cbf8-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7cbf8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cbf8-122">-ResourceGroupName</span></span>
<span data-ttu-id="7cbf8-123">指定包含此 Cmdlet 移除之公用 IP 位址之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7cbf8-123">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7cbf8-124">-確認</span><span class="sxs-lookup"><span data-stu-id="7cbf8-124">-Confirm</span></span>
<span data-ttu-id="7cbf8-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7cbf8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cbf8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cbf8-126">-WhatIf</span></span>
<span data-ttu-id="7cbf8-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7cbf8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cbf8-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7cbf8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cbf8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cbf8-129">CommonParameters</span></span>
<span data-ttu-id="7cbf8-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7cbf8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cbf8-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7cbf8-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cbf8-132">輸入</span><span class="sxs-lookup"><span data-stu-id="7cbf8-132">INPUTS</span></span>

### <span data-ttu-id="7cbf8-133">System.object</span><span class="sxs-lookup"><span data-stu-id="7cbf8-133">System.String</span></span>

## <span data-ttu-id="7cbf8-134">輸出</span><span class="sxs-lookup"><span data-stu-id="7cbf8-134">OUTPUTS</span></span>

### <span data-ttu-id="7cbf8-135">System.object</span><span class="sxs-lookup"><span data-stu-id="7cbf8-135">System.Boolean</span></span>

## <span data-ttu-id="7cbf8-136">筆記</span><span class="sxs-lookup"><span data-stu-id="7cbf8-136">NOTES</span></span>

## <span data-ttu-id="7cbf8-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="7cbf8-137">RELATED LINKS</span></span>

[<span data-ttu-id="7cbf8-138">AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7cbf8-138">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="7cbf8-139">新-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7cbf8-139">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="7cbf8-140">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7cbf8-140">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


