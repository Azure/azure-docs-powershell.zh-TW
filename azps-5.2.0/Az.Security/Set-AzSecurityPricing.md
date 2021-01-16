---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
ms.openlocfilehash: 96f5a9d4791dc2668e4ec82abc140f17cbce7c44
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281052"
---
# <span data-ttu-id="d9f9e-101">Set-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="d9f9e-101">Set-AzSecurityPricing</span></span>

## <span data-ttu-id="d9f9e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d9f9e-102">SYNOPSIS</span></span>

<span data-ttu-id="d9f9e-103">啟用或停用 Azure 安全中心訂閱的 Azure Defender 方案。</span><span class="sxs-lookup"><span data-stu-id="d9f9e-103">Enables or disables Azure Defender plans for a subscription in Azure Security Center.</span></span>

## <span data-ttu-id="d9f9e-104">句法</span><span class="sxs-lookup"><span data-stu-id="d9f9e-104">SYNTAX</span></span>

### <span data-ttu-id="d9f9e-105">SubscriptionLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="d9f9e-105">SubscriptionLevelResource (Default)</span></span>

```powershell
Set-AzSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9f9e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d9f9e-106">InputObject</span></span>

```powershell
Set-AzSecurityPricing -InputObject <PSSecurityPricing> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9f9e-107">說明</span><span class="sxs-lookup"><span data-stu-id="d9f9e-107">DESCRIPTION</span></span>

<span data-ttu-id="d9f9e-108">啟用或停用任何訂閱的 Azure Defender 方案。</span><span class="sxs-lookup"><span data-stu-id="d9f9e-108">Enable or disable any of the Azure Defender plans for a subscription.</span></span>

<span data-ttu-id="d9f9e-109">如需 Azure Defender 和可用方案的詳細資訊，請參閱 [Azure Defender 簡介](https://docs.microsoft.com/azure/security-center/azure-defender)。</span><span class="sxs-lookup"><span data-stu-id="d9f9e-109">For details about Azure Defender and the available plans, see [Introduction to Azure Defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span></span>

## <span data-ttu-id="d9f9e-110">示例</span><span class="sxs-lookup"><span data-stu-id="d9f9e-110">EXAMPLES</span></span>

### <span data-ttu-id="d9f9e-111">範例1</span><span class="sxs-lookup"><span data-stu-id="d9f9e-111">Example 1</span></span>

```powershell
PS C:\> Set-AzSecurityPricing -Name "virtualmachines" -PricingTier "Standard"
```

<span data-ttu-id="d9f9e-112">為 **伺服器啟用 Azure Defender** for 訂閱。</span><span class="sxs-lookup"><span data-stu-id="d9f9e-112">Enables **Azure Defender for servers** for the subscription.</span></span>

<span data-ttu-id="d9f9e-113">"標準" 指的是 azure Defender 方案的「開啟」狀態，如 azure 安全中心的 azure 入口網站的 [定價] 和 [設定] 區域所示。</span><span class="sxs-lookup"><span data-stu-id="d9f9e-113">"Standard" refers to the "On" state for an Azure Defender plan as shown in Azure Security Center's pricing and settings area of the Azure portal.</span></span>


## <span data-ttu-id="d9f9e-114">參數</span><span class="sxs-lookup"><span data-stu-id="d9f9e-114">PARAMETERS</span></span>

### <span data-ttu-id="d9f9e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9f9e-115">-DefaultProfile</span></span>

<span data-ttu-id="d9f9e-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d9f9e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9f9e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9f9e-117">-InputObject</span></span>

<span data-ttu-id="d9f9e-118">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="d9f9e-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9f9e-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="d9f9e-119">-Name</span></span>

<span data-ttu-id="d9f9e-120">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="d9f9e-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9f9e-121">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="d9f9e-121">-PricingTier</span></span>

<span data-ttu-id="d9f9e-122">定價層。</span><span class="sxs-lookup"><span data-stu-id="d9f9e-122">Pricing Tier.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9f9e-123">-確認</span><span class="sxs-lookup"><span data-stu-id="d9f9e-123">-Confirm</span></span>

<span data-ttu-id="d9f9e-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d9f9e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9f9e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9f9e-125">-WhatIf</span></span>

<span data-ttu-id="d9f9e-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d9f9e-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d9f9e-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d9f9e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9f9e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9f9e-128">CommonParameters</span></span>

<span data-ttu-id="d9f9e-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d9f9e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9f9e-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d9f9e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9f9e-131">輸入</span><span class="sxs-lookup"><span data-stu-id="d9f9e-131">INPUTS</span></span>

### <span data-ttu-id="d9f9e-132">PSSecurityPricing 中的 Pricings （Security..。</span><span class="sxs-lookup"><span data-stu-id="d9f9e-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="d9f9e-133">輸出</span><span class="sxs-lookup"><span data-stu-id="d9f9e-133">OUTPUTS</span></span>

### <span data-ttu-id="d9f9e-134">PSSecurityPricing 中的 Pricings （Security..。</span><span class="sxs-lookup"><span data-stu-id="d9f9e-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="d9f9e-135">筆記</span><span class="sxs-lookup"><span data-stu-id="d9f9e-135">NOTES</span></span>

## <span data-ttu-id="d9f9e-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="d9f9e-136">RELATED LINKS</span></span>
