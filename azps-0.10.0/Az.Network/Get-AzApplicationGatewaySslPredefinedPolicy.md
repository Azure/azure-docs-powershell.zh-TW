---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslpredefinedpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslPredefinedPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslPredefinedPolicy.md
ms.openlocfilehash: 2c55da6b7193d02de51e273df4626152d6d088fb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794447"
---
# <span data-ttu-id="53a18-101">Get-AzApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="53a18-101">Get-AzApplicationGatewaySslPredefinedPolicy</span></span>

## <span data-ttu-id="53a18-102">摘要</span><span class="sxs-lookup"><span data-stu-id="53a18-102">SYNOPSIS</span></span>
<span data-ttu-id="53a18-103">取得由應用程式閘道提供的預先定義 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="53a18-103">Gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="53a18-104">句法</span><span class="sxs-lookup"><span data-stu-id="53a18-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPredefinedPolicy [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="53a18-105">說明</span><span class="sxs-lookup"><span data-stu-id="53a18-105">DESCRIPTION</span></span>
<span data-ttu-id="53a18-106">**AzApplicationGatewaySslPredefinedPolicy** Cmdlet 會取得由應用程式閘道提供的預先定義 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="53a18-106">The **Get-AzApplicationGatewaySslPredefinedPolicy** cmdlet gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="53a18-107">示例</span><span class="sxs-lookup"><span data-stu-id="53a18-107">EXAMPLES</span></span>

### <span data-ttu-id="53a18-108">範例1</span><span class="sxs-lookup"><span data-stu-id="53a18-108">Example 1</span></span>
```
PS C:\>$policies = Get-AzApplicationGatewaySslPredefinedPolicy
```

<span data-ttu-id="53a18-109">這個命令會傳回所有預先定義的 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="53a18-109">This commands returns all the predefined SSL policies.</span></span>

### <span data-ttu-id="53a18-110">範例2</span><span class="sxs-lookup"><span data-stu-id="53a18-110">Example 2</span></span>
```
PS C:\>$policy = Get-AzApplicationGatewaySslPredefinedPolicy -Name AppGwSslPolicy20170401
```

<span data-ttu-id="53a18-111">這個命令會傳回預先定義的原則與 name AppGwSslPolicy20170401。</span><span class="sxs-lookup"><span data-stu-id="53a18-111">This commands returns predefined policy with name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="53a18-112">參數</span><span class="sxs-lookup"><span data-stu-id="53a18-112">PARAMETERS</span></span>

### <span data-ttu-id="53a18-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53a18-113">-DefaultProfile</span></span>
<span data-ttu-id="53a18-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="53a18-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53a18-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="53a18-115">-Name</span></span>
<span data-ttu-id="53a18-116">Ssl 預先定義原則的名稱</span><span class="sxs-lookup"><span data-stu-id="53a18-116">Name of the ssl predefined policy</span></span>

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

### <span data-ttu-id="53a18-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53a18-117">CommonParameters</span></span>
<span data-ttu-id="53a18-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="53a18-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53a18-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="53a18-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53a18-120">輸入</span><span class="sxs-lookup"><span data-stu-id="53a18-120">INPUTS</span></span>

### <span data-ttu-id="53a18-121">所有</span><span class="sxs-lookup"><span data-stu-id="53a18-121">None</span></span>

## <span data-ttu-id="53a18-122">輸出</span><span class="sxs-lookup"><span data-stu-id="53a18-122">OUTPUTS</span></span>

### <span data-ttu-id="53a18-123">PSApplicationGatewaySslPredefinedPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="53a18-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy</span></span>
<span data-ttu-id="53a18-124">[System.object]. IEnumerable "1 [PSApplicationGatewaySslPredefinedPolicy，4.1.0.0，network，版本 =，Culture = 中性，PublicKeyToken = null]] （Culture = null）]</span><span class="sxs-lookup"><span data-stu-id="53a18-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="53a18-125">筆記</span><span class="sxs-lookup"><span data-stu-id="53a18-125">NOTES</span></span>

## <span data-ttu-id="53a18-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="53a18-126">RELATED LINKS</span></span>

