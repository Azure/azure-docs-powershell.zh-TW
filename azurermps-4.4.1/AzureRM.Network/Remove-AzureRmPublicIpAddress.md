---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpAddress.md
ms.openlocfilehash: 396f603c4a4126b8d438f0048677da7a5dbd7492
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449606"
---
# <span data-ttu-id="b55bb-101">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b55bb-101">Remove-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="b55bb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b55bb-102">SYNOPSIS</span></span>
<span data-ttu-id="b55bb-103">移除公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="b55bb-103">Removes a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b55bb-104">句法</span><span class="sxs-lookup"><span data-stu-id="b55bb-104">SYNTAX</span></span>

```
Remove-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b55bb-105">說明</span><span class="sxs-lookup"><span data-stu-id="b55bb-105">DESCRIPTION</span></span>
<span data-ttu-id="b55bb-106">**AzureRmPublicIpAddress** Cmdlet 會移除 AZURE 公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="b55bb-106">The **Remove-AzureRmPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="b55bb-107">示例</span><span class="sxs-lookup"><span data-stu-id="b55bb-107">EXAMPLES</span></span>

### <span data-ttu-id="b55bb-108">1：移除公用 IP 位址資源</span><span class="sxs-lookup"><span data-stu-id="b55bb-108">1: Remove a public IP address resource</span></span>
```
Remove-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="b55bb-109">這個命令會移除 [資源] 群組 $rgName 中名為 $publicIpName 的公用 IP 位址資源。</span><span class="sxs-lookup"><span data-stu-id="b55bb-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="b55bb-110">參數</span><span class="sxs-lookup"><span data-stu-id="b55bb-110">PARAMETERS</span></span>

### <span data-ttu-id="b55bb-111">-Force</span><span class="sxs-lookup"><span data-stu-id="b55bb-111">-Force</span></span>
<span data-ttu-id="b55bb-112">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b55bb-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b55bb-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="b55bb-113">-Name</span></span>
<span data-ttu-id="b55bb-114">指定此 Cmdlet 移除之公用 IP 位址的名稱。</span><span class="sxs-lookup"><span data-stu-id="b55bb-114">Specifies the name of the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b55bb-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b55bb-115">-PassThru</span></span>
<span data-ttu-id="b55bb-116">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="b55bb-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b55bb-117">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="b55bb-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b55bb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b55bb-118">-ResourceGroupName</span></span>
<span data-ttu-id="b55bb-119">指定包含此 Cmdlet 移除之公用 IP 位址之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b55bb-119">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b55bb-120">-確認</span><span class="sxs-lookup"><span data-stu-id="b55bb-120">-Confirm</span></span>
<span data-ttu-id="b55bb-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b55bb-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b55bb-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b55bb-122">-WhatIf</span></span>
<span data-ttu-id="b55bb-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b55bb-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b55bb-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b55bb-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b55bb-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b55bb-125">-DefaultProfile</span></span>
<span data-ttu-id="b55bb-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b55bb-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b55bb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b55bb-127">CommonParameters</span></span>
<span data-ttu-id="b55bb-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b55bb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b55bb-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b55bb-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b55bb-130">輸入</span><span class="sxs-lookup"><span data-stu-id="b55bb-130">INPUTS</span></span>

## <span data-ttu-id="b55bb-131">輸出</span><span class="sxs-lookup"><span data-stu-id="b55bb-131">OUTPUTS</span></span>

## <span data-ttu-id="b55bb-132">筆記</span><span class="sxs-lookup"><span data-stu-id="b55bb-132">NOTES</span></span>

## <span data-ttu-id="b55bb-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="b55bb-133">RELATED LINKS</span></span>

[<span data-ttu-id="b55bb-134">AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b55bb-134">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="b55bb-135">新-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b55bb-135">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="b55bb-136">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b55bb-136">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


