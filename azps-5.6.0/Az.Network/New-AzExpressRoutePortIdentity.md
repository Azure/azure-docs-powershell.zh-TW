---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
ms.openlocfilehash: e3b3b0a0990f8c72fcd18d8828ae97d5c1a8a5aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917682"
---
# <span data-ttu-id="e10de-101">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="e10de-101">New-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="e10de-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e10de-102">SYNOPSIS</span></span>
<span data-ttu-id="e10de-103">建立 Azure ExpressRoutePortIdentity。</span><span class="sxs-lookup"><span data-stu-id="e10de-103">Creates an Azure ExpressRoutePortIdentity.</span></span>

## <span data-ttu-id="e10de-104">語法</span><span class="sxs-lookup"><span data-stu-id="e10de-104">SYNTAX</span></span>

```
New-AzExpressRoutePortIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e10de-105">描述</span><span class="sxs-lookup"><span data-stu-id="e10de-105">DESCRIPTION</span></span>
<span data-ttu-id="e10de-106">**New-AzExpressRoutePortIdentity Cmdlet** 會建立一個本地 Azure ExpressRoutePort Identity 物件。</span><span class="sxs-lookup"><span data-stu-id="e10de-106">The **New-AzExpressRoutePortIdentity** cmdlet creates a local Azure ExpressRoutePort Identity object.</span></span> <span data-ttu-id="e10de-107">使用 **New-AzExpressRoutePort** 或 **Set-AzExpressRoutePort** 將其指派給 Azure ExpressRoutePort。</span><span class="sxs-lookup"><span data-stu-id="e10de-107">Use **New-AzExpressRoutePort** or **Set-AzExpressRoutePort** to assign it to Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="e10de-108">例子</span><span class="sxs-lookup"><span data-stu-id="e10de-108">EXAMPLES</span></span>

### <span data-ttu-id="e10de-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="e10de-109">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    UserAssignedIdentityId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.ManagedIdentity/userAssignedIdentities/<IdentityName>'
    }
PS C:\> New-AzExpressRoutePortIdentity @parameters
```

## <span data-ttu-id="e10de-110">參數</span><span class="sxs-lookup"><span data-stu-id="e10de-110">PARAMETERS</span></span>

### <span data-ttu-id="e10de-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e10de-111">-DefaultProfile</span></span>
<span data-ttu-id="e10de-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e10de-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e10de-113">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="e10de-113">-UserAssignedIdentityId</span></span>
<span data-ttu-id="e10de-114">指派身分識別給使用者的 ResourceId，指派給 ExpressRoutePort。</span><span class="sxs-lookup"><span data-stu-id="e10de-114">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

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

### <span data-ttu-id="e10de-115">-確認</span><span class="sxs-lookup"><span data-stu-id="e10de-115">-Confirm</span></span>
<span data-ttu-id="e10de-116">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e10de-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e10de-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e10de-117">-WhatIf</span></span>
<span data-ttu-id="e10de-118">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e10de-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e10de-119">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e10de-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e10de-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e10de-120">CommonParameters</span></span>
<span data-ttu-id="e10de-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e10de-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e10de-122">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="e10de-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e10de-123">輸入</span><span class="sxs-lookup"><span data-stu-id="e10de-123">INPUTS</span></span>

### <span data-ttu-id="e10de-124">System.String</span><span class="sxs-lookup"><span data-stu-id="e10de-124">System.String</span></span>

## <span data-ttu-id="e10de-125">輸出</span><span class="sxs-lookup"><span data-stu-id="e10de-125">OUTPUTS</span></span>

### <span data-ttu-id="e10de-126">Microsoft.Azure.Commands.Network.models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="e10de-126">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="e10de-127">筆記</span><span class="sxs-lookup"><span data-stu-id="e10de-127">NOTES</span></span>

## <span data-ttu-id="e10de-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="e10de-128">RELATED LINKS</span></span>
[<span data-ttu-id="e10de-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="e10de-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="e10de-130">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="e10de-130">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="e10de-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="e10de-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)