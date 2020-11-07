---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysslpredefinedpolicy
schema: 2.0.0
ms.openlocfilehash: a977de2b4a60f0fc5ae93e175d521d398d40f850
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802386"
---
# <span data-ttu-id="1c669-101">Get-AzureRmApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="1c669-101">Get-AzureRmApplicationGatewaySslPredefinedPolicy</span></span>

## <span data-ttu-id="1c669-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1c669-102">SYNOPSIS</span></span>
<span data-ttu-id="1c669-103">取得由應用程式閘道提供的預先定義 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="1c669-103">Gets Predefined SSL Policies provided by Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c669-104">句法</span><span class="sxs-lookup"><span data-stu-id="1c669-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslPredefinedPolicy [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1c669-105">說明</span><span class="sxs-lookup"><span data-stu-id="1c669-105">DESCRIPTION</span></span>
<span data-ttu-id="1c669-106">**AzureRmApplicationGatewaySslPredefinedPolicy** Cmdlet 會取得由應用程式閘道提供的預先定義 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="1c669-106">The **Get-AzureRmApplicationGatewaySslPredefinedPolicy** cmdlet gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="1c669-107">示例</span><span class="sxs-lookup"><span data-stu-id="1c669-107">EXAMPLES</span></span>

### <span data-ttu-id="1c669-108">範例1</span><span class="sxs-lookup"><span data-stu-id="1c669-108">Example 1</span></span>
```
PS C:\>$policies = Get-AzureRmApplicationGatewaySslPredefinedPolicy
```

<span data-ttu-id="1c669-109">這個命令會傳回所有預先定義的 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="1c669-109">This commands returns all the predefined SSL policies.</span></span>

### <span data-ttu-id="1c669-110">範例2</span><span class="sxs-lookup"><span data-stu-id="1c669-110">Example 2</span></span>
```
PS C:\>$policy = Get-AzureRmApplicationGatewaySslPredefinedPolicy -Name AppGwSslPolicy20170401
```

<span data-ttu-id="1c669-111">這個命令會傳回預先定義的原則與 name AppGwSslPolicy20170401。</span><span class="sxs-lookup"><span data-stu-id="1c669-111">This commands returns predefined policy with name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="1c669-112">參數</span><span class="sxs-lookup"><span data-stu-id="1c669-112">PARAMETERS</span></span>

### <span data-ttu-id="1c669-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c669-113">-DefaultProfile</span></span>
<span data-ttu-id="1c669-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1c669-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c669-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="1c669-115">-Name</span></span>
<span data-ttu-id="1c669-116">Ssl 預先定義原則的名稱</span><span class="sxs-lookup"><span data-stu-id="1c669-116">Name of the ssl predefined policy</span></span>

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

### <span data-ttu-id="1c669-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c669-117">CommonParameters</span></span>
<span data-ttu-id="1c669-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1c669-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c669-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1c669-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c669-120">輸入</span><span class="sxs-lookup"><span data-stu-id="1c669-120">INPUTS</span></span>

### <span data-ttu-id="1c669-121">所有</span><span class="sxs-lookup"><span data-stu-id="1c669-121">None</span></span>

## <span data-ttu-id="1c669-122">輸出</span><span class="sxs-lookup"><span data-stu-id="1c669-122">OUTPUTS</span></span>

### <span data-ttu-id="1c669-123">PSApplicationGatewaySslPredefinedPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1c669-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy</span></span>
<span data-ttu-id="1c669-124">[System.object]. IEnumerable "1 [PSApplicationGatewaySslPredefinedPolicy，4.1.0.0，network，版本 =，Culture = 中性，PublicKeyToken = null]] （Culture = null）]</span><span class="sxs-lookup"><span data-stu-id="1c669-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="1c669-125">筆記</span><span class="sxs-lookup"><span data-stu-id="1c669-125">NOTES</span></span>

## <span data-ttu-id="1c669-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="1c669-126">RELATED LINKS</span></span>

