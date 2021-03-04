---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
ms.openlocfilehash: 6292c2fd19ff61e347291d3aba7e9840799e3b93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908062"
---
# <span data-ttu-id="e99e1-101">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="e99e1-101">Set-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="e99e1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e99e1-102">SYNOPSIS</span></span>
<span data-ttu-id="e99e1-103">更新指派給 ExpressRoutePort 的身分識別。</span><span class="sxs-lookup"><span data-stu-id="e99e1-103">Updates a identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="e99e1-104">語法</span><span class="sxs-lookup"><span data-stu-id="e99e1-104">SYNTAX</span></span>

```
Set-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e99e1-105">描述</span><span class="sxs-lookup"><span data-stu-id="e99e1-105">DESCRIPTION</span></span>
<span data-ttu-id="e99e1-106">**Set-AzExpressRoutePortIdentity Cmdlet** 會更新一個本地 Azure ExpressRoutePort 物件。</span><span class="sxs-lookup"><span data-stu-id="e99e1-106">The **Set-AzExpressRoutePortIdentity** cmdlet updates a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="e99e1-107">使用 **Set-AzExpressRoutePort** 將其指派給 ExpressRoutePort。</span><span class="sxs-lookup"><span data-stu-id="e99e1-107">Use **Set-AzExpressRoutePort** to assign it to ExpressRoutePort.</span></span>

## <span data-ttu-id="e99e1-108">例子</span><span class="sxs-lookup"><span data-stu-id="e99e1-108">EXAMPLES</span></span>

### <span data-ttu-id="e99e1-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="e99e1-109">Example 1</span></span>
```powershell
PS C:\>$exrport = Get-AzExpressRoutePort -Name $portName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$exrPortIdentity = Set-AzExpressRoutePortIdentity -UserAssignedIdentity $identity.Id -ExpressRoutePort $exrPort
PS C:\>$updatedExrPort = Set-AzExpressRoutePort -ExpressRoutePort $exrPort
```

## <span data-ttu-id="e99e1-110">參數</span><span class="sxs-lookup"><span data-stu-id="e99e1-110">PARAMETERS</span></span>

### <span data-ttu-id="e99e1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e99e1-111">-DefaultProfile</span></span>
<span data-ttu-id="e99e1-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e99e1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e99e1-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="e99e1-113">-ExpressRoutePort</span></span>
<span data-ttu-id="e99e1-114">The ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="e99e1-114">The ExpressRoutePort</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e99e1-115">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="e99e1-115">-UserAssignedIdentityId</span></span>
<span data-ttu-id="e99e1-116">指派身分識別給使用者的 ResourceId，指派給 ExpressRoutePort。</span><span class="sxs-lookup"><span data-stu-id="e99e1-116">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

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

### <span data-ttu-id="e99e1-117">-確認</span><span class="sxs-lookup"><span data-stu-id="e99e1-117">-Confirm</span></span>
<span data-ttu-id="e99e1-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e99e1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e99e1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e99e1-119">-WhatIf</span></span>
<span data-ttu-id="e99e1-120">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e99e1-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e99e1-121">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e99e1-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e99e1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e99e1-122">CommonParameters</span></span>
<span data-ttu-id="e99e1-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e99e1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e99e1-124">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="e99e1-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e99e1-125">輸入</span><span class="sxs-lookup"><span data-stu-id="e99e1-125">INPUTS</span></span>

### <span data-ttu-id="e99e1-126">Microsoft.Azure.Commands.Network.models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="e99e1-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="e99e1-127">System.String</span><span class="sxs-lookup"><span data-stu-id="e99e1-127">System.String</span></span>

## <span data-ttu-id="e99e1-128">輸出</span><span class="sxs-lookup"><span data-stu-id="e99e1-128">OUTPUTS</span></span>

### <span data-ttu-id="e99e1-129">Microsoft.Azure.Commands.Network.models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="e99e1-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="e99e1-130">筆記</span><span class="sxs-lookup"><span data-stu-id="e99e1-130">NOTES</span></span>

## <span data-ttu-id="e99e1-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="e99e1-131">RELATED LINKS</span></span>
[<span data-ttu-id="e99e1-132">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="e99e1-132">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="e99e1-133">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="e99e1-133">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="e99e1-134">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="e99e1-134">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)
