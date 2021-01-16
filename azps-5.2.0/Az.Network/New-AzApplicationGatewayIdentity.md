---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
ms.openlocfilehash: e32c0912026555f9b85a83720d1c7c48a5170f70
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280501"
---
# <span data-ttu-id="1b2f1-101">New-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="1b2f1-101">New-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="1b2f1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1b2f1-102">SYNOPSIS</span></span>
<span data-ttu-id="1b2f1-103">為應用程式閘道建立身分識別物件。</span><span class="sxs-lookup"><span data-stu-id="1b2f1-103">Creates an identity object for an application gateway.</span></span> <span data-ttu-id="1b2f1-104">這將會保留使用者指派身分識別的參照。</span><span class="sxs-lookup"><span data-stu-id="1b2f1-104">This will hold reference to the user assigned identity.</span></span>

## <span data-ttu-id="1b2f1-105">句法</span><span class="sxs-lookup"><span data-stu-id="1b2f1-105">SYNTAX</span></span>

```
New-AzApplicationGatewayIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b2f1-106">說明</span><span class="sxs-lookup"><span data-stu-id="1b2f1-106">DESCRIPTION</span></span>
<span data-ttu-id="1b2f1-107">**AzApplicationGatewayIdentity** Cmdlet 會建立應用程式閘道身分識別物件。</span><span class="sxs-lookup"><span data-stu-id="1b2f1-107">**New-AzApplicationGatewayIdentity** cmdlet creates an application gateway identity object.</span></span>

## <span data-ttu-id="1b2f1-108">示例</span><span class="sxs-lookup"><span data-stu-id="1b2f1-108">EXAMPLES</span></span>

### <span data-ttu-id="1b2f1-109">範例1</span><span class="sxs-lookup"><span data-stu-id="1b2f1-109">Example 1</span></span>
```powershell
PS C:\> $identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\> $appgwIdentity = New-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id
PS C:\> $gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -Identity $appgwIdentity <..>
```

<span data-ttu-id="1b2f1-110">在這個範例中，我們會建立一個指派身分識別的使用者，然後在與應用程式閘道搭配使用的身分識別物件中引用它。</span><span class="sxs-lookup"><span data-stu-id="1b2f1-110">In this example, we create a user assigned identity and then reference it in identity object used with Application Gateway.</span></span>

## <span data-ttu-id="1b2f1-111">參數</span><span class="sxs-lookup"><span data-stu-id="1b2f1-111">PARAMETERS</span></span>

### <span data-ttu-id="1b2f1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b2f1-112">-DefaultProfile</span></span>
<span data-ttu-id="1b2f1-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b2f1-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b2f1-114">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="1b2f1-114">-UserAssignedIdentityId</span></span>
<span data-ttu-id="1b2f1-115">指派給應用程式閘道的使用者指派身分識別的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="1b2f1-115">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="1b2f1-116">-確認</span><span class="sxs-lookup"><span data-stu-id="1b2f1-116">-Confirm</span></span>
<span data-ttu-id="1b2f1-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1b2f1-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b2f1-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b2f1-118">-WhatIf</span></span>
<span data-ttu-id="1b2f1-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1b2f1-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b2f1-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1b2f1-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b2f1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b2f1-121">CommonParameters</span></span>
<span data-ttu-id="1b2f1-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1b2f1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b2f1-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1b2f1-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b2f1-124">輸入</span><span class="sxs-lookup"><span data-stu-id="1b2f1-124">INPUTS</span></span>

### <span data-ttu-id="1b2f1-125">System.object</span><span class="sxs-lookup"><span data-stu-id="1b2f1-125">System.String</span></span>

## <span data-ttu-id="1b2f1-126">輸出</span><span class="sxs-lookup"><span data-stu-id="1b2f1-126">OUTPUTS</span></span>

### <span data-ttu-id="1b2f1-127">PSManagedServiceIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1b2f1-127">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="1b2f1-128">筆記</span><span class="sxs-lookup"><span data-stu-id="1b2f1-128">NOTES</span></span>

## <span data-ttu-id="1b2f1-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="1b2f1-129">RELATED LINKS</span></span>
