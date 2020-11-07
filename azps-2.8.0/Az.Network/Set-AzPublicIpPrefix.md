---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
ms.openlocfilehash: caa0baf8e26ea2cec94a59bd2a86e6394b4ade91
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791593"
---
# <span data-ttu-id="82d98-101">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="82d98-101">Set-AzPublicIpPrefix</span></span>

## <span data-ttu-id="82d98-102">摘要</span><span class="sxs-lookup"><span data-stu-id="82d98-102">SYNOPSIS</span></span>
<span data-ttu-id="82d98-103">設定現有 PublicIpPrefix 的標記</span><span class="sxs-lookup"><span data-stu-id="82d98-103">Sets the Tags for an existing PublicIpPrefix</span></span>

## <span data-ttu-id="82d98-104">句法</span><span class="sxs-lookup"><span data-stu-id="82d98-104">SYNTAX</span></span>

```
Set-AzPublicIpPrefix -PublicIpPrefix <PSPublicIpPrefix> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82d98-105">說明</span><span class="sxs-lookup"><span data-stu-id="82d98-105">DESCRIPTION</span></span>
<span data-ttu-id="82d98-106">**AzPublicIpPrefix** Cmdlet 會設定公用 IP 首碼的標記。</span><span class="sxs-lookup"><span data-stu-id="82d98-106">The **Set-AzPublicIpPrefix** cmdlet sets the Tags for a public IP prefix.</span></span>

## <span data-ttu-id="82d98-107">示例</span><span class="sxs-lookup"><span data-stu-id="82d98-107">EXAMPLES</span></span>

### <span data-ttu-id="82d98-108">設定公用 ip 首碼的標記</span><span class="sxs-lookup"><span data-stu-id="82d98-108">Set the tags for public ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName

PS C:\> $publicIpPrefix.Tags = "TestTag"

PS C:\> Set-AzPublicIpPrefix -PublicIpPrefix $publicIpPrefix
```

<span data-ttu-id="82d98-109">第一個命令會取得現有的公用 IP 首碼，第二個命令會設定 Tags 屬性，而第三個命令會更新現有的物件。</span><span class="sxs-lookup"><span data-stu-id="82d98-109">The first command gets an existing public IP Prefix, the second command sets the Tags Property and the third command updates the existing object.</span></span>

## <span data-ttu-id="82d98-110">參數</span><span class="sxs-lookup"><span data-stu-id="82d98-110">PARAMETERS</span></span>

### <span data-ttu-id="82d98-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82d98-111">-AsJob</span></span>
<span data-ttu-id="82d98-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82d98-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="82d98-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82d98-113">-DefaultProfile</span></span>
<span data-ttu-id="82d98-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="82d98-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82d98-115">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="82d98-115">-PublicIpPrefix</span></span>
<span data-ttu-id="82d98-116">PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="82d98-116">The PublicIpPrefix</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82d98-117">-確認</span><span class="sxs-lookup"><span data-stu-id="82d98-117">-Confirm</span></span>
<span data-ttu-id="82d98-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="82d98-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82d98-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82d98-119">-WhatIf</span></span>
<span data-ttu-id="82d98-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="82d98-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82d98-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="82d98-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82d98-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82d98-122">CommonParameters</span></span>
<span data-ttu-id="82d98-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="82d98-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82d98-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="82d98-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82d98-125">輸入</span><span class="sxs-lookup"><span data-stu-id="82d98-125">INPUTS</span></span>

### <span data-ttu-id="82d98-126">PSPublicIpPrefix 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="82d98-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="82d98-127">輸出</span><span class="sxs-lookup"><span data-stu-id="82d98-127">OUTPUTS</span></span>

### <span data-ttu-id="82d98-128">PSPublicIpPrefix 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="82d98-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="82d98-129">筆記</span><span class="sxs-lookup"><span data-stu-id="82d98-129">NOTES</span></span>

## <span data-ttu-id="82d98-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="82d98-130">RELATED LINKS</span></span>

[<span data-ttu-id="82d98-131">AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="82d98-131">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="82d98-132">新-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="82d98-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="82d98-133">移除-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="82d98-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)
