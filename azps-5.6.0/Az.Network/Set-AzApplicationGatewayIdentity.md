---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 2f100d29b2251d71b170c7833f77ab2f23f90209
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902865"
---
# <span data-ttu-id="99bfe-101">Set-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="99bfe-101">Set-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="99bfe-102">簡介</span><span class="sxs-lookup"><span data-stu-id="99bfe-102">SYNOPSIS</span></span>
<span data-ttu-id="99bfe-103">更新指派給應用程式閘道的身分識別。</span><span class="sxs-lookup"><span data-stu-id="99bfe-103">Updates a identity assigned to the application gateway.</span></span>

## <span data-ttu-id="99bfe-104">語法</span><span class="sxs-lookup"><span data-stu-id="99bfe-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99bfe-105">描述</span><span class="sxs-lookup"><span data-stu-id="99bfe-105">DESCRIPTION</span></span>
<span data-ttu-id="99bfe-106">**Set-AzApplicationGatewayIdentity** Cmdlet 會更新指派給應用程式閘道的身分識別。</span><span class="sxs-lookup"><span data-stu-id="99bfe-106">The **Set-AzApplicationGatewayIdentity** cmdlet updates an identity assigned to application gateway.</span></span>

## <span data-ttu-id="99bfe-107">例子</span><span class="sxs-lookup"><span data-stu-id="99bfe-107">EXAMPLES</span></span>

### <span data-ttu-id="99bfe-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="99bfe-108">Example 1</span></span>
```powershell
PS C:\>$appgw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$appgwIdentity = Set-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id -ApplicationGateway $appgw
PS C:\>$updatedAppGw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="99bfe-109">在此範例中，我們會指派使用者身分識別給現有的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="99bfe-109">In this example, we assign a user assigned identity to an existing application gateway.</span></span>
<span data-ttu-id="99bfe-110">注意：此身分識別應可存取要參照憑證/機密的 keyvault。</span><span class="sxs-lookup"><span data-stu-id="99bfe-110">Note: This identity should have access to the keyvault from which the certificates/secrets will be referenced.</span></span>

## <span data-ttu-id="99bfe-111">參數</span><span class="sxs-lookup"><span data-stu-id="99bfe-111">PARAMETERS</span></span>

### <span data-ttu-id="99bfe-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99bfe-112">-ApplicationGateway</span></span>
<span data-ttu-id="99bfe-113">應用程式Gateway</span><span class="sxs-lookup"><span data-stu-id="99bfe-113">The applicationGateway</span></span>

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

### <span data-ttu-id="99bfe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99bfe-114">-DefaultProfile</span></span>
<span data-ttu-id="99bfe-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="99bfe-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99bfe-116">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="99bfe-116">-UserAssignedIdentityId</span></span>
<span data-ttu-id="99bfe-117">指派身分識別給使用者的 ResourceId，指派給應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="99bfe-117">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: UserAssignedIdentity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99bfe-118">-確認</span><span class="sxs-lookup"><span data-stu-id="99bfe-118">-Confirm</span></span>
<span data-ttu-id="99bfe-119">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="99bfe-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99bfe-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99bfe-120">-WhatIf</span></span>
<span data-ttu-id="99bfe-121">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="99bfe-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99bfe-122">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="99bfe-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99bfe-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99bfe-123">CommonParameters</span></span>
<span data-ttu-id="99bfe-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="99bfe-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99bfe-125">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="99bfe-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99bfe-126">輸入</span><span class="sxs-lookup"><span data-stu-id="99bfe-126">INPUTS</span></span>

### <span data-ttu-id="99bfe-127">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99bfe-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="99bfe-128">System.String</span><span class="sxs-lookup"><span data-stu-id="99bfe-128">System.String</span></span>

## <span data-ttu-id="99bfe-129">輸出</span><span class="sxs-lookup"><span data-stu-id="99bfe-129">OUTPUTS</span></span>

### <span data-ttu-id="99bfe-130">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99bfe-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="99bfe-131">筆記</span><span class="sxs-lookup"><span data-stu-id="99bfe-131">NOTES</span></span>

## <span data-ttu-id="99bfe-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="99bfe-132">RELATED LINKS</span></span>
