---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: ecd5a8eafc70a88b4ebda17a83f2b40139f5463f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624361"
---
# <span data-ttu-id="00058-101">Set-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="00058-101">Set-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="00058-102">摘要</span><span class="sxs-lookup"><span data-stu-id="00058-102">SYNOPSIS</span></span>
<span data-ttu-id="00058-103">{{填入摘要}}</span><span class="sxs-lookup"><span data-stu-id="00058-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00058-104">句法</span><span class="sxs-lookup"><span data-stu-id="00058-104">SYNTAX</span></span>

```
Set-AzureRmServiceEndpointPolicy -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00058-105">說明</span><span class="sxs-lookup"><span data-stu-id="00058-105">DESCRIPTION</span></span>
<span data-ttu-id="00058-106">**AzureRmServiceEndpointPolicy** Cmdlet 會建立服務端點原則。</span><span class="sxs-lookup"><span data-stu-id="00058-106">The **Set-AzureRmServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="00058-107">示例</span><span class="sxs-lookup"><span data-stu-id="00058-107">EXAMPLES</span></span>

### <span data-ttu-id="00058-108">範例1：設定服務端點原則</span><span class="sxs-lookup"><span data-stu-id="00058-108">Example 1: Sets a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzureRmServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicy $serviceEndpointPolicy -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="00058-109">這個命令會更新物件所定義的名為 Policy1 的服務端點原則，$serviceEndpointPolicy 屬於該 resourcegroup "resourcegroup1"。</span><span class="sxs-lookup"><span data-stu-id="00058-109">This command updates a service endpoint policy named Policy1 defined by the object $serviceEndpointPolicy belong to the resourcegroup "resourcegroup1".</span></span>

## <span data-ttu-id="00058-110">參數</span><span class="sxs-lookup"><span data-stu-id="00058-110">PARAMETERS</span></span>

### <span data-ttu-id="00058-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00058-111">-DefaultProfile</span></span>
<span data-ttu-id="00058-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="00058-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00058-113">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="00058-113">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="00058-114">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="00058-114">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="00058-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00058-115">CommonParameters</span></span>
<span data-ttu-id="00058-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="00058-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="00058-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="00058-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00058-118">輸入</span><span class="sxs-lookup"><span data-stu-id="00058-118">INPUTS</span></span>

### <span data-ttu-id="00058-119">PSServiceEndpointPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="00058-119">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="00058-120">輸出</span><span class="sxs-lookup"><span data-stu-id="00058-120">OUTPUTS</span></span>

### <span data-ttu-id="00058-121">PSServiceEndpointPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="00058-121">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="00058-122">筆記</span><span class="sxs-lookup"><span data-stu-id="00058-122">NOTES</span></span>

## <span data-ttu-id="00058-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="00058-123">RELATED LINKS</span></span>
