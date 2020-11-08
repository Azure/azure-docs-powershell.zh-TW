---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
ms.openlocfilehash: 07a29a17a1a7c17a0bbf7b202b019e7d833a5050
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139384"
---
# <span data-ttu-id="4ad27-101">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="4ad27-101">Set-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="4ad27-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4ad27-102">SYNOPSIS</span></span>
<span data-ttu-id="4ad27-103">儲存已修改的 Azure SecurityPartnerProvider。</span><span class="sxs-lookup"><span data-stu-id="4ad27-103">Saves a modified Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="4ad27-104">句法</span><span class="sxs-lookup"><span data-stu-id="4ad27-104">SYNTAX</span></span>

```
Set-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ad27-105">說明</span><span class="sxs-lookup"><span data-stu-id="4ad27-105">DESCRIPTION</span></span>
<span data-ttu-id="4ad27-106">**AzSecurityPartnerProvider** Cmdlet 會更新 Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="4ad27-106">The **Set-AzSecurityPartnerProvider** cmdlet updates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="4ad27-107">示例</span><span class="sxs-lookup"><span data-stu-id="4ad27-107">EXAMPLES</span></span>

### <span data-ttu-id="4ad27-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4ad27-108">Example 1</span></span>
```powershell
$securityPartnerProvider = Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
Set-AzSecurityPartnerProvider -SecurityPartnerProvider $securityPartnerProvider
```


## <span data-ttu-id="4ad27-109">參數</span><span class="sxs-lookup"><span data-stu-id="4ad27-109">PARAMETERS</span></span>

### <span data-ttu-id="4ad27-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ad27-110">-AsJob</span></span>
<span data-ttu-id="4ad27-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4ad27-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4ad27-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ad27-112">-DefaultProfile</span></span>
<span data-ttu-id="4ad27-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4ad27-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ad27-114">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="4ad27-114">-SecurityPartnerProvider</span></span>
<span data-ttu-id="4ad27-115">SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="4ad27-115">The SecurityPartnerProvider</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ad27-116">-確認</span><span class="sxs-lookup"><span data-stu-id="4ad27-116">-Confirm</span></span>
<span data-ttu-id="4ad27-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4ad27-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ad27-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ad27-118">-WhatIf</span></span>
<span data-ttu-id="4ad27-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4ad27-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ad27-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4ad27-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ad27-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ad27-121">CommonParameters</span></span>
<span data-ttu-id="4ad27-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4ad27-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ad27-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4ad27-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ad27-124">輸入</span><span class="sxs-lookup"><span data-stu-id="4ad27-124">INPUTS</span></span>

### <span data-ttu-id="4ad27-125">PSSecurityPartnerProvider 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4ad27-125">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="4ad27-126">輸出</span><span class="sxs-lookup"><span data-stu-id="4ad27-126">OUTPUTS</span></span>

### <span data-ttu-id="4ad27-127">PSSecurityPartnerProvider 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4ad27-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="4ad27-128">筆記</span><span class="sxs-lookup"><span data-stu-id="4ad27-128">NOTES</span></span>

## <span data-ttu-id="4ad27-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="4ad27-129">RELATED LINKS</span></span>
