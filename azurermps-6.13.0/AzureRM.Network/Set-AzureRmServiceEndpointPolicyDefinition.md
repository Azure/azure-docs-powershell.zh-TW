---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 1348eff2e4a2ac755ac0f425ddb29816438199b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624360"
---
# <span data-ttu-id="3b1c3-101">Set-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3b1c3-101">Set-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="3b1c3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3b1c3-102">SYNOPSIS</span></span>
<span data-ttu-id="3b1c3-103">{{填入摘要}}</span><span class="sxs-lookup"><span data-stu-id="3b1c3-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b1c3-104">句法</span><span class="sxs-lookup"><span data-stu-id="3b1c3-104">SYNTAX</span></span>

```
Set-AzureRmServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <System.Collections.Generic.List`1[System.String]>]
 [-Service <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b1c3-105">說明</span><span class="sxs-lookup"><span data-stu-id="3b1c3-105">DESCRIPTION</span></span>
<span data-ttu-id="3b1c3-106">**AzureRmServiceEndpointPolicyDefinition** Cmdlet 會建立服務端點原則定義。</span><span class="sxs-lookup"><span data-stu-id="3b1c3-106">The **Set-AzureRmServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="3b1c3-107">示例</span><span class="sxs-lookup"><span data-stu-id="3b1c3-107">EXAMPLES</span></span>

### <span data-ttu-id="3b1c3-108">範例1：更新服務端點原則中的服務端點原則定義</span><span class="sxs-lookup"><span data-stu-id="3b1c3-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzureRmServiceEndpointPolicyDefinition -Name "Policydef1" -ServiceEndpointPolicy $serviceEndpointPolicy
```

<span data-ttu-id="3b1c3-109">這個命令會更新 $ServiceEndpointPolicy 物件定義之服務端點原則中名為 Policydef1 的服務端點原則定義。</span><span class="sxs-lookup"><span data-stu-id="3b1c3-109">This command updates a service endpoint policy definition named Policydef1 in the service endpoint policy defined by the object $ServiceEndpointPolicy.</span></span>

## <span data-ttu-id="3b1c3-110">參數</span><span class="sxs-lookup"><span data-stu-id="3b1c3-110">PARAMETERS</span></span>

### <span data-ttu-id="3b1c3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b1c3-111">-DefaultProfile</span></span>
<span data-ttu-id="3b1c3-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3b1c3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b1c3-113">-描述</span><span class="sxs-lookup"><span data-stu-id="3b1c3-113">-Description</span></span>
<span data-ttu-id="3b1c3-114">定義的描述</span><span class="sxs-lookup"><span data-stu-id="3b1c3-114">The description of the definition</span></span>

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

### <span data-ttu-id="3b1c3-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="3b1c3-115">-Name</span></span>
<span data-ttu-id="3b1c3-116">規則名稱</span><span class="sxs-lookup"><span data-stu-id="3b1c3-116">The name of the rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b1c3-117">-服務</span><span class="sxs-lookup"><span data-stu-id="3b1c3-117">-Service</span></span>
<span data-ttu-id="3b1c3-118">服務名稱</span><span class="sxs-lookup"><span data-stu-id="3b1c3-118">Name of the service</span></span>

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

### <span data-ttu-id="3b1c3-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="3b1c3-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="3b1c3-120">NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3b1c3-120">The NetworkSecurityGroup</span></span>

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

### <span data-ttu-id="3b1c3-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="3b1c3-121">-ServiceResource</span></span>
<span data-ttu-id="3b1c3-122">服務資源清單</span><span class="sxs-lookup"><span data-stu-id="3b1c3-122">List of service resources</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b1c3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b1c3-123">CommonParameters</span></span>
<span data-ttu-id="3b1c3-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3b1c3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3b1c3-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3b1c3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b1c3-126">輸入</span><span class="sxs-lookup"><span data-stu-id="3b1c3-126">INPUTS</span></span>

### <span data-ttu-id="3b1c3-127">PSServiceEndpointPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3b1c3-127">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="3b1c3-128">輸出</span><span class="sxs-lookup"><span data-stu-id="3b1c3-128">OUTPUTS</span></span>

### <span data-ttu-id="3b1c3-129">PSServiceEndpointPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3b1c3-129">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="3b1c3-130">筆記</span><span class="sxs-lookup"><span data-stu-id="3b1c3-130">NOTES</span></span>

## <span data-ttu-id="3b1c3-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="3b1c3-131">RELATED LINKS</span></span>
