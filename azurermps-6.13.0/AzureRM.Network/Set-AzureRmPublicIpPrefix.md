---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpPrefix.md
ms.openlocfilehash: 7b60c157f3e86e72461c82f34a2d23dcb5eb0b20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443771"
---
# <span data-ttu-id="0c192-101">Set-AzureRmPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0c192-101">Set-AzureRmPublicIpPrefix</span></span>

## <span data-ttu-id="0c192-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0c192-102">SYNOPSIS</span></span>
<span data-ttu-id="0c192-103">設定現有 PublicIpPrefix 的標記</span><span class="sxs-lookup"><span data-stu-id="0c192-103">Sets the Tags for an existing PublicIpPrefix</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c192-104">句法</span><span class="sxs-lookup"><span data-stu-id="0c192-104">SYNTAX</span></span>

```
Set-AzureRmPublicIpPrefix -PublicIpPrefix <PSPublicIpPrefix> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c192-105">說明</span><span class="sxs-lookup"><span data-stu-id="0c192-105">DESCRIPTION</span></span>
<span data-ttu-id="0c192-106">**AzureRmPublicIpPrefix** Cmdlet 會設定公用 IP 首碼的標記。</span><span class="sxs-lookup"><span data-stu-id="0c192-106">The **Set-AzureRmPublicIpPrefix** cmdlet sets the Tags for a public IP prefix.</span></span>

## <span data-ttu-id="0c192-107">示例</span><span class="sxs-lookup"><span data-stu-id="0c192-107">EXAMPLES</span></span>

### <span data-ttu-id="0c192-108">設定公用 ip 首碼的標記</span><span class="sxs-lookup"><span data-stu-id="0c192-108">Set the tags for public ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzureRmPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName

PS C:\> $publicIpPrefix.Tags = "TestTag"

PS C:\> Set-AzureRmPublicIpPrefix -PublicIpPrefix $publicIpPrefix
```

<span data-ttu-id="0c192-109">第一個命令會取得現有的公用 IP 首碼，第二個命令會設定 Tags 屬性，而第三個命令會更新現有的物件。</span><span class="sxs-lookup"><span data-stu-id="0c192-109">The first command gets an existing public IP Prefix, the second command sets the Tags Property and the third command updates the existing object.</span></span>

## <span data-ttu-id="0c192-110">參數</span><span class="sxs-lookup"><span data-stu-id="0c192-110">PARAMETERS</span></span>

### <span data-ttu-id="0c192-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c192-111">-AsJob</span></span>
<span data-ttu-id="0c192-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0c192-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0c192-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c192-113">-DefaultProfile</span></span>
<span data-ttu-id="0c192-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0c192-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c192-115">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0c192-115">-PublicIpPrefix</span></span>
<span data-ttu-id="0c192-116">PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0c192-116">The PublicIpPrefix</span></span>

```yaml
Type: PSPublicIpPrefix
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c192-117">-確認</span><span class="sxs-lookup"><span data-stu-id="0c192-117">-Confirm</span></span>
<span data-ttu-id="0c192-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0c192-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c192-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c192-119">-WhatIf</span></span>
<span data-ttu-id="0c192-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0c192-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c192-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0c192-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c192-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c192-122">CommonParameters</span></span>
<span data-ttu-id="0c192-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0c192-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="0c192-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0c192-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c192-125">輸入</span><span class="sxs-lookup"><span data-stu-id="0c192-125">INPUTS</span></span>

### <span data-ttu-id="0c192-126">PSPublicIpPrefix 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0c192-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="0c192-127">輸出</span><span class="sxs-lookup"><span data-stu-id="0c192-127">OUTPUTS</span></span>

### <span data-ttu-id="0c192-128">PSPublicIpPrefix 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0c192-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="0c192-129">筆記</span><span class="sxs-lookup"><span data-stu-id="0c192-129">NOTES</span></span>

## <span data-ttu-id="0c192-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="0c192-130">RELATED LINKS</span></span>