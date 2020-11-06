---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 83a44e97e01e846cec568227514177babd76d30a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621495"
---
# <span data-ttu-id="09bcf-101">Set-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="09bcf-101">Set-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="09bcf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="09bcf-102">SYNOPSIS</span></span>
<span data-ttu-id="09bcf-103">更新指派給應用程式閘道的身分識別。</span><span class="sxs-lookup"><span data-stu-id="09bcf-103">Updates a identity assigned to the application gateway.</span></span>

## <span data-ttu-id="09bcf-104">句法</span><span class="sxs-lookup"><span data-stu-id="09bcf-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09bcf-105">說明</span><span class="sxs-lookup"><span data-stu-id="09bcf-105">DESCRIPTION</span></span>
<span data-ttu-id="09bcf-106">**AzApplicationGatewayIdentity** Cmdlet 會更新指派給應用程式閘道的身分識別。</span><span class="sxs-lookup"><span data-stu-id="09bcf-106">The **Set-AzApplicationGatewayIdentity** cmdlet updates an identity assigned to application gateway.</span></span>

## <span data-ttu-id="09bcf-107">示例</span><span class="sxs-lookup"><span data-stu-id="09bcf-107">EXAMPLES</span></span>

### <span data-ttu-id="09bcf-108">範例1</span><span class="sxs-lookup"><span data-stu-id="09bcf-108">Example 1</span></span>
```powershell
PS C:\>$appgw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$appgwIdentity = Set-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id -ApplicationGateway $appgw
PS C:\>$updatedAppGw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="09bcf-109">在這個範例中，我們會將指派身分識別的使用者指派給現有的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="09bcf-109">In this example, we assign a user assigned identity to an existing applicaiton gateway.</span></span>
<span data-ttu-id="09bcf-110">注意：此身分識別應該有權存取將會參照其憑證/密碼的 keyvault。</span><span class="sxs-lookup"><span data-stu-id="09bcf-110">Note: This identity should have access to the keyvault from which the certificates/secrets will be referenced.</span></span>

## <span data-ttu-id="09bcf-111">參數</span><span class="sxs-lookup"><span data-stu-id="09bcf-111">PARAMETERS</span></span>

### <span data-ttu-id="09bcf-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="09bcf-112">-ApplicationGateway</span></span>
<span data-ttu-id="09bcf-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="09bcf-113">The applicationGateway</span></span>

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

### <span data-ttu-id="09bcf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09bcf-114">-DefaultProfile</span></span>
<span data-ttu-id="09bcf-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="09bcf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09bcf-116">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="09bcf-116">-UserAssignedIdentityId</span></span>
<span data-ttu-id="09bcf-117">指派給應用程式閘道的使用者指派身分識別的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="09bcf-117">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="09bcf-118">-確認</span><span class="sxs-lookup"><span data-stu-id="09bcf-118">-Confirm</span></span>
<span data-ttu-id="09bcf-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="09bcf-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09bcf-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09bcf-120">-WhatIf</span></span>
<span data-ttu-id="09bcf-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="09bcf-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09bcf-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="09bcf-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09bcf-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09bcf-123">CommonParameters</span></span>
<span data-ttu-id="09bcf-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="09bcf-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09bcf-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="09bcf-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09bcf-126">輸入</span><span class="sxs-lookup"><span data-stu-id="09bcf-126">INPUTS</span></span>

### <span data-ttu-id="09bcf-127">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="09bcf-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="09bcf-128">System.object</span><span class="sxs-lookup"><span data-stu-id="09bcf-128">System.String</span></span>

## <span data-ttu-id="09bcf-129">輸出</span><span class="sxs-lookup"><span data-stu-id="09bcf-129">OUTPUTS</span></span>

### <span data-ttu-id="09bcf-130">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="09bcf-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="09bcf-131">筆記</span><span class="sxs-lookup"><span data-stu-id="09bcf-131">NOTES</span></span>

## <span data-ttu-id="09bcf-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="09bcf-132">RELATED LINKS</span></span>
