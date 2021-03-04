---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
ms.openlocfilehash: f1cc98c8008d8f9eff47fa6f5172fb28a448c7ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912710"
---
# <span data-ttu-id="30ea6-101">New-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="30ea6-101">New-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="30ea6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="30ea6-102">SYNOPSIS</span></span>
<span data-ttu-id="30ea6-103">為應用程式閘道建立身分識別物件。</span><span class="sxs-lookup"><span data-stu-id="30ea6-103">Creates an identity object for an application gateway.</span></span> <span data-ttu-id="30ea6-104">這會保留使用者指派身分識別的參照。</span><span class="sxs-lookup"><span data-stu-id="30ea6-104">This will hold reference to the user assigned identity.</span></span>

## <span data-ttu-id="30ea6-105">語法</span><span class="sxs-lookup"><span data-stu-id="30ea6-105">SYNTAX</span></span>

```
New-AzApplicationGatewayIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30ea6-106">描述</span><span class="sxs-lookup"><span data-stu-id="30ea6-106">DESCRIPTION</span></span>
<span data-ttu-id="30ea6-107">**New-AzApplicationGatewayIdentity** Cmdlet 會建立應用程式閘道身分識別物件。</span><span class="sxs-lookup"><span data-stu-id="30ea6-107">**New-AzApplicationGatewayIdentity** cmdlet creates an application gateway identity object.</span></span>

## <span data-ttu-id="30ea6-108">例子</span><span class="sxs-lookup"><span data-stu-id="30ea6-108">EXAMPLES</span></span>

### <span data-ttu-id="30ea6-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="30ea6-109">Example 1</span></span>
```powershell
PS C:\> $identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\> $appgwIdentity = New-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id
PS C:\> $gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -Identity $appgwIdentity <..>
```

<span data-ttu-id="30ea6-110">在此範例中，我們會建立使用者指派的身分識別，然後在與應用程式閘道一起使用的身分識別物件中參照。</span><span class="sxs-lookup"><span data-stu-id="30ea6-110">In this example, we create a user assigned identity and then reference it in identity object used with Application Gateway.</span></span>

## <span data-ttu-id="30ea6-111">參數</span><span class="sxs-lookup"><span data-stu-id="30ea6-111">PARAMETERS</span></span>

### <span data-ttu-id="30ea6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30ea6-112">-DefaultProfile</span></span>
<span data-ttu-id="30ea6-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="30ea6-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30ea6-114">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="30ea6-114">-UserAssignedIdentityId</span></span>
<span data-ttu-id="30ea6-115">指派身分識別給使用者的 ResourceId，指派給應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="30ea6-115">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="30ea6-116">-確認</span><span class="sxs-lookup"><span data-stu-id="30ea6-116">-Confirm</span></span>
<span data-ttu-id="30ea6-117">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="30ea6-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30ea6-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30ea6-118">-WhatIf</span></span>
<span data-ttu-id="30ea6-119">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="30ea6-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30ea6-120">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30ea6-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30ea6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30ea6-121">CommonParameters</span></span>
<span data-ttu-id="30ea6-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="30ea6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30ea6-123">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="30ea6-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30ea6-124">輸入</span><span class="sxs-lookup"><span data-stu-id="30ea6-124">INPUTS</span></span>

### <span data-ttu-id="30ea6-125">System.String</span><span class="sxs-lookup"><span data-stu-id="30ea6-125">System.String</span></span>

## <span data-ttu-id="30ea6-126">輸出</span><span class="sxs-lookup"><span data-stu-id="30ea6-126">OUTPUTS</span></span>

### <span data-ttu-id="30ea6-127">Microsoft.Azure.Commands.Network.models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="30ea6-127">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="30ea6-128">筆記</span><span class="sxs-lookup"><span data-stu-id="30ea6-128">NOTES</span></span>

## <span data-ttu-id="30ea6-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="30ea6-129">RELATED LINKS</span></span>
