---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 2ba4a6c0f625941daf34b6754a3df856b8554075
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274135"
---
# <span data-ttu-id="8d740-101">Get-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="8d740-101">Get-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="8d740-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8d740-102">SYNOPSIS</span></span>
<span data-ttu-id="8d740-103">取得指派給應用程式閘道的身分識別。</span><span class="sxs-lookup"><span data-stu-id="8d740-103">Get identity assigned to the application gateway.</span></span>

## <span data-ttu-id="8d740-104">句法</span><span class="sxs-lookup"><span data-stu-id="8d740-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d740-105">說明</span><span class="sxs-lookup"><span data-stu-id="8d740-105">DESCRIPTION</span></span>
<span data-ttu-id="8d740-106">**AzApplicationGatewayIdentity** Cmdlet 會取得指派給應用程式閘道的身分識別。</span><span class="sxs-lookup"><span data-stu-id="8d740-106">The **Get-AzApplicationGatewayIdentity** cmdlet gets identity assigned to the application gateway.</span></span>

## <span data-ttu-id="8d740-107">示例</span><span class="sxs-lookup"><span data-stu-id="8d740-107">EXAMPLES</span></span>

### <span data-ttu-id="8d740-108">範例1</span><span class="sxs-lookup"><span data-stu-id="8d740-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzApplicationGatewayIdentity -ApplicationGateway $gw
```

<span data-ttu-id="8d740-109">此範例說明如何從應用程式閘道取得應用程式閘道身分識別。</span><span class="sxs-lookup"><span data-stu-id="8d740-109">This examples shows how to get application gateway identity from Application Gateway.</span></span>

## <span data-ttu-id="8d740-110">參數</span><span class="sxs-lookup"><span data-stu-id="8d740-110">PARAMETERS</span></span>

### <span data-ttu-id="8d740-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8d740-111">-ApplicationGateway</span></span>
<span data-ttu-id="8d740-112">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8d740-112">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d740-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d740-113">-DefaultProfile</span></span>
<span data-ttu-id="8d740-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8d740-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d740-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d740-115">CommonParameters</span></span>
<span data-ttu-id="8d740-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8d740-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d740-117">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8d740-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d740-118">輸入</span><span class="sxs-lookup"><span data-stu-id="8d740-118">INPUTS</span></span>

### <span data-ttu-id="8d740-119">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8d740-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8d740-120">輸出</span><span class="sxs-lookup"><span data-stu-id="8d740-120">OUTPUTS</span></span>

### <span data-ttu-id="8d740-121">PSManagedServiceIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8d740-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="8d740-122">筆記</span><span class="sxs-lookup"><span data-stu-id="8d740-122">NOTES</span></span>

## <span data-ttu-id="8d740-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="8d740-123">RELATED LINKS</span></span>
