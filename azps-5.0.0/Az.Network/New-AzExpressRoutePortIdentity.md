---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
ms.openlocfilehash: d19acf8bb97f3b84b3cd831e4cf91397231f4b08
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139990"
---
# <span data-ttu-id="7c4f2-101">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="7c4f2-101">New-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="7c4f2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7c4f2-102">SYNOPSIS</span></span>
<span data-ttu-id="7c4f2-103">建立 Azure ExpressRoutePortIdentity。</span><span class="sxs-lookup"><span data-stu-id="7c4f2-103">Creates an Azure ExpressRoutePortIdentity.</span></span>

## <span data-ttu-id="7c4f2-104">句法</span><span class="sxs-lookup"><span data-stu-id="7c4f2-104">SYNTAX</span></span>

```
New-AzExpressRoutePortIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c4f2-105">說明</span><span class="sxs-lookup"><span data-stu-id="7c4f2-105">DESCRIPTION</span></span>
<span data-ttu-id="7c4f2-106">**新的-AzExpressRoutePortIdentity** Cmdlet 會建立一個本機 Azure ExpressRoutePort 身分識別物件。</span><span class="sxs-lookup"><span data-stu-id="7c4f2-106">The **New-AzExpressRoutePortIdentity** cmdlet creates a local Azure ExpressRoutePort Identity object.</span></span> <span data-ttu-id="7c4f2-107">使用 **新的 AzExpressRoutePort** 或 **AzExpressRoutePort** 將其指派給 Azure ExpressRoutePort。</span><span class="sxs-lookup"><span data-stu-id="7c4f2-107">Use **New-AzExpressRoutePort** or **Set-AzExpressRoutePort** to assign it to Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="7c4f2-108">示例</span><span class="sxs-lookup"><span data-stu-id="7c4f2-108">EXAMPLES</span></span>

### <span data-ttu-id="7c4f2-109">範例1</span><span class="sxs-lookup"><span data-stu-id="7c4f2-109">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    UserAssignedIdentityId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.ManagedIdentity/userAssignedIdentities/<IdentityName>'
    }
PS C:\> New-AzExpressRoutePortIdentity @parameters
```

## <span data-ttu-id="7c4f2-110">參數</span><span class="sxs-lookup"><span data-stu-id="7c4f2-110">PARAMETERS</span></span>

### <span data-ttu-id="7c4f2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c4f2-111">-DefaultProfile</span></span>
<span data-ttu-id="7c4f2-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7c4f2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c4f2-113">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="7c4f2-113">-UserAssignedIdentityId</span></span>
<span data-ttu-id="7c4f2-114">指派給 ExpressRoutePort 的使用者指派身分識別的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="7c4f2-114">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

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

### <span data-ttu-id="7c4f2-115">-確認</span><span class="sxs-lookup"><span data-stu-id="7c4f2-115">-Confirm</span></span>
<span data-ttu-id="7c4f2-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7c4f2-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c4f2-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c4f2-117">-WhatIf</span></span>
<span data-ttu-id="7c4f2-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7c4f2-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c4f2-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7c4f2-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c4f2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c4f2-120">CommonParameters</span></span>
<span data-ttu-id="7c4f2-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7c4f2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c4f2-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7c4f2-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c4f2-123">輸入</span><span class="sxs-lookup"><span data-stu-id="7c4f2-123">INPUTS</span></span>

### <span data-ttu-id="7c4f2-124">System.object</span><span class="sxs-lookup"><span data-stu-id="7c4f2-124">System.String</span></span>

## <span data-ttu-id="7c4f2-125">輸出</span><span class="sxs-lookup"><span data-stu-id="7c4f2-125">OUTPUTS</span></span>

### <span data-ttu-id="7c4f2-126">PSManagedServiceIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7c4f2-126">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="7c4f2-127">筆記</span><span class="sxs-lookup"><span data-stu-id="7c4f2-127">NOTES</span></span>

## <span data-ttu-id="7c4f2-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="7c4f2-128">RELATED LINKS</span></span>
[<span data-ttu-id="7c4f2-129">AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="7c4f2-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="7c4f2-130">移除-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="7c4f2-130">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="7c4f2-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="7c4f2-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)