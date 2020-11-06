---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 3d406bf0dffb0ee250e1494fc05727d0a4c983ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455159"
---
# <span data-ttu-id="55952-101">Remove-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="55952-101">Remove-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="55952-102">摘要</span><span class="sxs-lookup"><span data-stu-id="55952-102">SYNOPSIS</span></span>
<span data-ttu-id="55952-103">{{填入摘要}}</span><span class="sxs-lookup"><span data-stu-id="55952-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55952-104">句法</span><span class="sxs-lookup"><span data-stu-id="55952-104">SYNTAX</span></span>

```
Remove-AzureRmServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55952-105">說明</span><span class="sxs-lookup"><span data-stu-id="55952-105">DESCRIPTION</span></span>
<span data-ttu-id="55952-106">**AzureRmServiceEndpointPolicy** Cmdlet 會移除服務端點原則。</span><span class="sxs-lookup"><span data-stu-id="55952-106">The **Remove-AzureRmServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="55952-107">示例</span><span class="sxs-lookup"><span data-stu-id="55952-107">EXAMPLES</span></span>

### <span data-ttu-id="55952-108">範例1：使用名稱移除服務端點原則</span><span class="sxs-lookup"><span data-stu-id="55952-108">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzureRmServiceEndpointPolicyDefinition -Name "PolicyDef1"
```

<span data-ttu-id="55952-109">這個命令會移除名稱為 PolicyDef1 的服務端點原則</span><span class="sxs-lookup"><span data-stu-id="55952-109">This command removes a service endpoint policy with name PolicyDef1</span></span>

## <span data-ttu-id="55952-110">參數</span><span class="sxs-lookup"><span data-stu-id="55952-110">PARAMETERS</span></span>

### <span data-ttu-id="55952-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55952-111">-DefaultProfile</span></span>
<span data-ttu-id="55952-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="55952-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55952-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="55952-113">-Name</span></span>
<span data-ttu-id="55952-114">服務端點定義的名稱</span><span class="sxs-lookup"><span data-stu-id="55952-114">The name of the service endpoint definition</span></span>

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

### <span data-ttu-id="55952-115">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="55952-115">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="55952-116">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="55952-116">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="55952-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55952-117">CommonParameters</span></span>
<span data-ttu-id="55952-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="55952-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="55952-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="55952-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55952-120">輸入</span><span class="sxs-lookup"><span data-stu-id="55952-120">INPUTS</span></span>

### <span data-ttu-id="55952-121">PSServiceEndpointPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="55952-121">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="55952-122">輸出</span><span class="sxs-lookup"><span data-stu-id="55952-122">OUTPUTS</span></span>

### <span data-ttu-id="55952-123">PSServiceEndpointPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="55952-123">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="55952-124">筆記</span><span class="sxs-lookup"><span data-stu-id="55952-124">NOTES</span></span>

## <span data-ttu-id="55952-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="55952-125">RELATED LINKS</span></span>
