---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 547b38fd30f09a305c63054b2f27d33db5ae6a86
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452775"
---
# <span data-ttu-id="2cce2-101">Get-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2cce2-101">Get-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="2cce2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2cce2-102">SYNOPSIS</span></span>
<span data-ttu-id="2cce2-103">{{填入摘要}}</span><span class="sxs-lookup"><span data-stu-id="2cce2-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2cce2-104">句法</span><span class="sxs-lookup"><span data-stu-id="2cce2-104">SYNTAX</span></span>

```
Get-AzureRmServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cce2-105">說明</span><span class="sxs-lookup"><span data-stu-id="2cce2-105">DESCRIPTION</span></span>
<span data-ttu-id="2cce2-106">**AzureRmServiceEndpointPolicyDefinition** Cmdlet 會取得服務端點原則定義。</span><span class="sxs-lookup"><span data-stu-id="2cce2-106">The **Get-AzureRmServiceEndpointPolicyDefinition** cmdlet gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="2cce2-107">示例</span><span class="sxs-lookup"><span data-stu-id="2cce2-107">EXAMPLES</span></span>

### <span data-ttu-id="2cce2-108">範例1</span><span class="sxs-lookup"><span data-stu-id="2cce2-108">Example 1</span></span>
```
$policydef= Get-AzureRmServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ServiceEndpointPolicy $Policy
```

<span data-ttu-id="2cce2-109">這個命令會在 ServiceEndpointPolicy 中取得名為 ServiceEndpointPolicyDefinition1 的服務端點原則定義，$Policy 將其儲存在 $policydef 變數中。</span><span class="sxs-lookup"><span data-stu-id="2cce2-109">This command gets the service endpoint policy definition named ServiceEndpointPolicyDefinition1 in ServiceEndpointPolicy $Policy stores it in the $policydef variable.</span></span>

## <span data-ttu-id="2cce2-110">參數</span><span class="sxs-lookup"><span data-stu-id="2cce2-110">PARAMETERS</span></span>

### <span data-ttu-id="2cce2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cce2-111">-DefaultProfile</span></span>
<span data-ttu-id="2cce2-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2cce2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cce2-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="2cce2-113">-Name</span></span>
<span data-ttu-id="2cce2-114">服務端點原則定義的名稱</span><span class="sxs-lookup"><span data-stu-id="2cce2-114">The name of the service endpoint policy definition</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cce2-115">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2cce2-115">-ResourceId</span></span>
<span data-ttu-id="2cce2-116">{{Fill ResourceId 描述}}</span><span class="sxs-lookup"><span data-stu-id="2cce2-116">{{Fill ResourceId Description}}</span></span>

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

### <span data-ttu-id="2cce2-117">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2cce2-117">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="2cce2-118">服務端點原則</span><span class="sxs-lookup"><span data-stu-id="2cce2-118">The Service endpoint policy</span></span>

```yaml
Type: PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cce2-119">-確認</span><span class="sxs-lookup"><span data-stu-id="2cce2-119">-Confirm</span></span>
<span data-ttu-id="2cce2-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2cce2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cce2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cce2-121">-WhatIf</span></span>
<span data-ttu-id="2cce2-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2cce2-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2cce2-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2cce2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cce2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cce2-124">CommonParameters</span></span>
<span data-ttu-id="2cce2-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2cce2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cce2-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2cce2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cce2-127">輸入</span><span class="sxs-lookup"><span data-stu-id="2cce2-127">INPUTS</span></span>

### <span data-ttu-id="2cce2-128">PSServiceEndpointPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2cce2-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="2cce2-129">輸出</span><span class="sxs-lookup"><span data-stu-id="2cce2-129">OUTPUTS</span></span>

### <span data-ttu-id="2cce2-130">PSServiceEndpointPolicyDefinition 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2cce2-130">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="2cce2-131">筆記</span><span class="sxs-lookup"><span data-stu-id="2cce2-131">NOTES</span></span>

## <span data-ttu-id="2cce2-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="2cce2-132">RELATED LINKS</span></span>
