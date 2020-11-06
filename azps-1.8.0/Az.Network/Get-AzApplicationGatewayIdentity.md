---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 96a170d302d66ed2fa27d2cd7bdb17fc23cefcd3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622089"
---
# <span data-ttu-id="beeb0-101">Get-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="beeb0-101">Get-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="beeb0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="beeb0-102">SYNOPSIS</span></span>
<span data-ttu-id="beeb0-103">取得指派給應用程式閘道的身分識別。</span><span class="sxs-lookup"><span data-stu-id="beeb0-103">Get identity assigned to the application gateway.</span></span>

## <span data-ttu-id="beeb0-104">句法</span><span class="sxs-lookup"><span data-stu-id="beeb0-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="beeb0-105">說明</span><span class="sxs-lookup"><span data-stu-id="beeb0-105">DESCRIPTION</span></span>
<span data-ttu-id="beeb0-106">**AzApplicationGatewayIdentity** Cmdlet 會取得指派給應用程式閘道的身分識別。</span><span class="sxs-lookup"><span data-stu-id="beeb0-106">The **Get-AzApplicationGatewayIdentity** cmdlet gets identity assigned to the application gateway.</span></span>

## <span data-ttu-id="beeb0-107">示例</span><span class="sxs-lookup"><span data-stu-id="beeb0-107">EXAMPLES</span></span>

### <span data-ttu-id="beeb0-108">範例1</span><span class="sxs-lookup"><span data-stu-id="beeb0-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzApplicationGatewayIdentity -ApplicationGateway $gw
```

<span data-ttu-id="beeb0-109">此範例說明如何從應用程式閘道取得應用程式閘道身分識別。</span><span class="sxs-lookup"><span data-stu-id="beeb0-109">This examples shows how to get application gateway identity from Application Gateway.</span></span>

## <span data-ttu-id="beeb0-110">參數</span><span class="sxs-lookup"><span data-stu-id="beeb0-110">PARAMETERS</span></span>

### <span data-ttu-id="beeb0-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="beeb0-111">-ApplicationGateway</span></span>
<span data-ttu-id="beeb0-112">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="beeb0-112">The applicationGateway</span></span>

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

### <span data-ttu-id="beeb0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beeb0-113">-DefaultProfile</span></span>
<span data-ttu-id="beeb0-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="beeb0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="beeb0-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beeb0-115">CommonParameters</span></span>
<span data-ttu-id="beeb0-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="beeb0-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beeb0-117">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="beeb0-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beeb0-118">輸入</span><span class="sxs-lookup"><span data-stu-id="beeb0-118">INPUTS</span></span>

### <span data-ttu-id="beeb0-119">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="beeb0-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="beeb0-120">輸出</span><span class="sxs-lookup"><span data-stu-id="beeb0-120">OUTPUTS</span></span>

### <span data-ttu-id="beeb0-121">PSManagedServiceIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="beeb0-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="beeb0-122">筆記</span><span class="sxs-lookup"><span data-stu-id="beeb0-122">NOTES</span></span>

## <span data-ttu-id="beeb0-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="beeb0-123">RELATED LINKS</span></span>
